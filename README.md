# Audio Storage for n8n WhatsApp Integration

This repository serves as static file storage for audio files used in n8n WhatsApp automation workflows.

## Directory Structure

```
storage/
├── audio/           # WhatsApp audio files (.ogg format recommended)
├── README.md        # This file
└── index.html       # Optional: Simple file listing page
```

## Usage

### For n8n Integration

Access files using GitHub raw URLs:
```
https://raw.githubusercontent.com/bilalod1-collab/storage/main/audio/filename.ogg
```

### Supported Audio Formats

- **OGG (Opus codec)**: Recommended for WhatsApp voice messages (appears as voice bubble 🎤)
- **MP3**: Will appear as file attachment with 📎 icon
- **OPUS**: Needs conversion to OGG for proper WhatsApp voice message display

### File Upload Methods

1. **GitHub Web Interface**: Drag and drop files directly
2. **Git Commands**: Clone, add files, commit, and push
3. **GitHub API**: Programmatic upload via n8n or other tools

## n8n Workflow Integration

1. Upload your audio files to the `/audio/` directory
2. Use HTTP Request node in n8n to fetch files:
   ```
   GET https://raw.githubusercontent.com/bilalod1-collab/storage/main/audio/your-file.ogg
   ```
3. Send to WhatsApp using Evolution API or WhatsApp Business API

## Notes

- Files are publicly accessible via GitHub raw URLs
- For WhatsApp voice messages, use OGG format with Opus codec
- Consider file naming conventions for easy n8n automation
- Repository size limit: 1GB per repository
