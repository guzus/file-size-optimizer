# Reduce File Size

A Claude Code command for compressing files using ffmpeg.

## Overview

This command reduces file sizes for images, videos, and audio files using ffmpeg compression techniques.

## Installation

1. Copy `reduce-file-size.md` to your Claude Code commands directory:

```bash
mkdir -p ~/.claude/commands
cp reduce-file-size.md ~/.claude/commands/
```

2. The command will be available immediately in Claude Code.

## Supported Formats

- **Images**: png, jpg, jpeg, webp, gif
- **Videos**: mp4, mov, mkv, avi, webm
- **Audio**: mp3, wav, flac, aac, m4a

## Usage

In Claude Code, run the command with:

```
/reduce-file-size <file-path> [target-size]
```

### Examples

```bash
# Compress an image to default 1MB
/reduce-file-size image.png

# Compress a video to 10MB
/reduce-file-size video.mp4 10mb

# Compress audio to 5MB
/reduce-file-size audio.wav 5mb
```

## Requirements

- [Claude Code](https://claude.com/claude-code) CLI installed
- ffmpeg installed on your system (`brew install ffmpeg` on macOS)

## License

MIT
