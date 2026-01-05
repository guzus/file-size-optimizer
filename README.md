# Reduce File Size

A Claude Code command for compressing files using ffmpeg.

## Overview

This command reduces file sizes for images, videos, and audio files using ffmpeg compression techniques.

## Supported Formats

- **Images**: png, jpg, jpeg, webp, gif
- **Videos**: mp4, mov, mkv, avi, webm
- **Audio**: mp3, wav, flac, aac, m4a

## Usage

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

- ffmpeg must be installed on your system

## License

MIT
