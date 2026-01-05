# Reduce File Size

Reduce the file size of the specified file using ffmpeg.

## Arguments
- `$ARGUMENTS` - Path to the file and optional target size (e.g., "image.png 1mb" or just "image.png")

## Instructions

Parse the arguments to extract:
1. The file path (required)
2. Target size (optional, default: 1MB)

Based on the file type, use the appropriate ffmpeg compression:

**For images (png, jpg, jpeg, webp, gif):**
- Convert to JPEG with quality adjustment
- Use `-q:v` to control quality (lower = better quality, 2-31 range)
- Start with quality 5, check size, adjust if needed
- Output as `{original-name}-compressed.jpg`

**For videos (mp4, mov, mkv, avi, webm):**
- Use H.264 codec with CRF for quality control
- Use `-crf` value (18-28 range, lower = better quality)
- Use `-preset medium` for balanced speed/compression
- Output as `{original-name}-compressed.mp4`

**For audio (mp3, wav, flac, aac, m4a):**
- Convert to MP3 with bitrate control
- Use `-b:a` to set bitrate (128k, 192k, etc.)
- Output as `{original-name}-compressed.mp3`

## Process

1. Check if the file exists
2. Get current file size
3. Determine file type from extension
4. Apply appropriate compression using ffmpeg
5. Verify the output is under target size
6. If still too large, apply more aggressive compression
7. Report original size, new size, and compression ratio
