# Video Note Taker with Timestamps

A lightweight, browser-based application for taking timestamped notes while watching videos. Perfect for educational content, lectures, tutorials, or any video where you need to capture key moments with their exact timestamps.

## Features

- **Timestamped Notes**: Add notes linked to specific video timestamps
- **Free-form Notes**: Add general notes without timestamps
- **Interactive Playback**: Click any timestamp to jump directly to that moment in the video
- **Edit & Delete**: Modify or remove notes after creation
- **Session Management**: Save and load your note-taking sessions
- **Export Options**:
  - Export as JSON for data portability
  - Export as PDF for sharing and printing
- **Transcript Integration**: Upload video transcripts in JSON format
- **Dark Theme**: Eye-friendly dark interface

## Getting Started

### Prerequisites

- A modern web browser (Chrome, Firefox, Safari, or Edge)
- Video files you want to annotate
- (Optional) Transcript files in JSON format

### Installation

No installation required! This is a standalone HTML file that runs entirely in your browser.

1. Clone this repository:
   ```bash
   git clone <repository-url>
   cd video-note-taker-with-timestamps
   ```

2. Open `index.html` in your web browser:
   ```bash
   open index.html
   ```
   Or simply double-click the `index.html` file.

### Quick Start

1. **Upload a Video**:
   - Click "Choose File" under "Upload Video"
   - Select your video file (supports .mp4, .mov, .avi, .webm, etc.)

2. **Upload a Transcript** (Optional):
   - Click "Choose File" under "Upload Transcript (JSON)"
   - Select your transcript JSON file
   - See the "Transcript Format" section below for the expected format

3. **Take Notes**:
   - Play your video and pause at any moment
   - Type your note in the text area
   - Click "Add Note at Current Time" to create a timestamped note
   - Or click "Add Note (No Timestamp)" for a free-form note

4. **Interact with Notes**:
   - Click any timestamp to jump to that moment in the video
   - Click "Edit" to modify a note
   - Click "Delete" to remove a note

5. **Export Your Work**:
   - Click "Export JSON" to save your session (can be reloaded later)
   - Click "Export PDF" to generate a printable document
   - Click "Load Session" to restore a previously saved session

## Transcript Format

The application expects transcript files in the following JSON format:

```json
{
  "segments": [
    {
      "start": 0,
      "end": 5000,
      "text": "Welcome to this video..."
    },
    {
      "start": 5000,
      "end": 10000,
      "text": "Today we'll be discussing..."
    }
  ]
}
```

Note: While transcript upload is supported, the current version displays video and accepts transcripts but doesn't yet show transcript text in the UI. This feature can be extended in future versions.

## Session File Format

Exported sessions are saved as JSON files with the following structure:

```json
{
  "videoFileName": "my-video.mp4",
  "transcriptFileName": "my-transcript.json",
  "notes": [
    {
      "timestamp": "00:01:23",
      "timestampMs": 83000,
      "text": "Important concept explained here",
      "id": 1699564801000,
      "type": "timestamped",
      "createdAt": 1699564801000
    }
  ],
  "exportDate": "2025-11-07T18:30:00.000Z"
}
```

## Keyboard Shortcuts

- **Cmd/Ctrl + Enter**: Add note at current timestamp (when typing in the note field)

## Project Structure

```
video-note-taker-with-timestamps/
├── index.html              # Main application file (HTML + CSS + JavaScript)
├── examples/              # Example files
│   ├── cut_the_chit_chat_with_artifacts.mov    # Sample video (not in git)
│   └── cut_the_chit_chat_with_artifacts.json   # Sample transcript
├── sessions/              # Saved note sessions
│   └── *.json            # Exported session files
├── pdf-exports/          # PDF exports
│   └── *.pdf            # Generated PDF files
├── sample_notes.json    # Example of a saved session
└── README.md           # This file
```

## Technical Details

- **Technology Stack**: Pure HTML5, CSS3, and vanilla JavaScript
- **No Dependencies**: No frameworks or libraries required
- **Client-Side Only**: All processing happens in your browser
- **Privacy**: Your videos and notes never leave your computer
- **File API**: Uses the browser's File API for reading local files
- **Blob URLs**: Creates temporary URLs for video playback

## Use Cases

- **Educational Videos**: Take structured notes while learning
- **Lectures**: Capture key points with timestamps
- **Tutorials**: Mark important steps and instructions
- **Interviews**: Annotate significant moments
- **Video Research**: Document findings with precise references
- **Content Review**: Create detailed notes for team collaboration

## Browser Compatibility

- Chrome/Edge: ✅ Full support
- Firefox: ✅ Full support
- Safari: ✅ Full support
- Opera: ✅ Full support

## Limitations

- Video files are loaded entirely in browser memory
- Very large video files (>2GB) may cause performance issues
- PDF export opens a print dialog (use "Save as PDF" in print options)
- Transcript text is not currently displayed in the UI (stored but not shown)

## Privacy & Security

- **100% Local**: All data processing happens in your browser
- **No Server**: No data is sent to any server
- **No Tracking**: No analytics or tracking scripts
- **No Account Required**: Use immediately without sign-up

## Future Enhancements

Potential features for future versions:
- Display transcript text synchronized with video playback
- Highlight transcript segments as video plays
- Search functionality for notes
- Tag/category system for notes
- Multiple export formats (Markdown, CSV)
- Cloud storage integration
- Video speed controls
- Note templates

## Contributing

Contributions are welcome! Feel free to:
- Report bugs
- Suggest new features
- Submit pull requests
- Improve documentation

## License

This project is open source and available for personal and commercial use.

## Support

If you encounter any issues or have questions, please open an issue on the GitHub repository.

---

Made with ❤️ for better video learning and annotation
