# Lecture Slides Processor

An Obsidian plugin for processing lecture PDFs into structured, searchable markdown notes with automatic linking.

## Features

- **PDF to Images**: Convert PDF slides to images for embedding
- **OCR Integration**: Extract text from slides using Mistral AI OCR
- **Automatic Structure**: Creates organized note structure with frontmatter
- **Hierarchical Linking**: Auto-creates and links Subject and Semester notes
- **Batch Processing**: Process multiple PDFs at once
- **Cleanup Tools**: Remove common boilerplate text (headers, footers, page numbers)

## Installation

1. Download the latest release
2. Extract to `.obsidian/plugins/lecture-slides/`
3. Enable the plugin in Obsidian settings
4. Configure your Mistral API key for OCR functionality

## Usage

### Process a PDF

1. Command palette: `Lecture Slides: Process PDF`
2. Select a PDF file from your vault
3. Configure output options (folder, naming)
4. The plugin creates:
   - Individual slide images
   - Markdown note with OCR text
   - Links to Subject and Semester notes

### Cleanup Existing Notes

1. Command palette: `Lecture Slides: Cleanup Marker Output`
2. Removes common boilerplate (university headers, page numbers, etc.)

## Output Structure

```
/Lectures
  /Subject Name
    /VL01
      VL01.md          # Main note with OCR text
      VL01_img-1.jpeg  # Slide images
      VL01_img-2.jpeg
    Subject.md         # Auto-created subject overview
  Semester.md          # Auto-created semester overview
```

## Configuration

- **Output Folder**: Where to save processed lectures
- **Image Format**: JPEG or PNG
- **OCR Provider**: Mistral AI (requires API key)
- **Auto-Link**: Create Subject/Semester notes automatically

## License

MIT License - see [LICENSE](LICENSE) for details.
