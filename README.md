# EmbedAI (PrivateGPT)

[![GitHub stars](https://img.shields.io/github/stars/SamurAIGPT/EmbedAI?style=social)](https://github.com/SamurAIGPT/EmbedAI/stargazers)
[![License](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)
[![Python 3.8+](https://img.shields.io/badge/python-3.8+-blue.svg)](https://www.python.org/downloads/)

Create a private QnA chatbot on your documents without relying on the internet. Leverage the power of local LLMs for complete privacy and security - none of your data ever leaves your local environment.

<img width="948" alt="EmbedAI Screenshot" src="https://github.com/SamurAIGPT/privateGPT/assets/4326215/76e24cd4-a890-4253-bb87-098c4f1328fd">

> Inspired by [imartinez/privateGPT](https://github.com/imartinez)

## Features

- **100% Private** - All processing happens locally. Your documents never leave your machine
- **No Internet Required** - Works completely offline after initial setup
- **Multiple Document Formats** - Support for PDF, TXT, DOC, DOCX, and more
- **Local LLM Support** - Uses GPT4All for local language model inference
- **Interactive UI** - Clean web interface for document upload and chat
- **Document Ingestion** - Automatic chunking and embedding of your documents
- **Source Citations** - See which parts of your documents informed each answer

## Quick Start

### Prerequisites

- Python 3.8 or later
- Node.js v18.12.1 or later
- Minimum 16GB RAM

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/SamurAIGPT/EmbedAI.git
   cd EmbedAI
   ```

2. **Start the client**
   ```bash
   cd client
   npm install
   npm run dev
   ```

3. **Start the server** (in a new terminal)
   ```bash
   cd server
   pip install -r requirements.txt
   python privateGPT.py
   ```

4. **Open the app**

   Navigate to http://localhost:3000 and click "Download Model" to get the required LLM.

## Architecture

```
EmbedAI/
├── client/          # Next.js frontend
│   ├── components/  # React components
│   └── pages/       # App pages
└── server/          # Python backend
    ├── privateGPT.py    # Main server
    └── ingest.py        # Document processing
```

## How It Works

1. **Upload Documents** - Drop your files into the web interface
2. **Automatic Processing** - Documents are chunked and embedded locally
3. **Ask Questions** - Chat naturally with your document corpus
4. **Get Answers** - Receive responses with source citations

## Supported File Types

| Format | Extension |
|--------|-----------|
| PDF | `.pdf` |
| Text | `.txt` |
| Word | `.doc`, `.docx` |
| Markdown | `.md` |

## Configuration

The default model is GPT4All. You can configure:
- Model selection
- Chunk size for document processing
- Number of source documents to retrieve

## Troubleshooting

**Model download fails?**
- Ensure you have a stable internet connection for the initial model download
- Check that you have enough disk space (~4GB for the model)

**Slow responses?**
- Local LLM inference requires significant CPU/RAM
- Consider using a machine with at least 16GB RAM

**Context window errors?**
- Try reducing the document chunk size
- Split large documents into smaller files

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## Follow for Updates

- [Anil Chandra Naidu Matcha](https://twitter.com/matchaman11)
- [Ankur Singh](https://twitter.com/ankur_maker)

## Related Projects

- [Open-Custom-GPT](https://github.com/SamurAIGPT/Open-Custom-GPT) - Build Custom GPTs with the Assistants API
- [Text-To-Video-AI](https://github.com/SamurAIGPT/Text-To-Video-AI) - Generate videos from text

## License

MIT License - see [LICENSE](LICENSE) for details.
