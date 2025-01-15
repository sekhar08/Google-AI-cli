# Google Generative AI CLI

This is a Node.js command-line interface (CLI) tool that interacts with the Google Generative AI API to generate content based on user input. The tool allows you to ask questions directly or provide context from files, directories, or PDFs.

## Installation

To install this package, you need to have Node.js and npm installed. You can install the package globally using npm:

```sh
npm install -g gen-ai-chat
```

## Usage

### Basic Usage

To ask a question directly from the command line:

```sh
npx gen-ai-chat "Your question here"
```

### Using a File for Context

To provide additional context from a file, use the `-f` flag followed by the file path:

```sh
npx gen-ai-chat "Your question here" -f /path/to/your/file.txt
```

### Using a Directory for Context

To provide additional context from all files in a directory, use the `-d` flag followed by the directory path:

```sh
npx gen-ai-chat "Your question here" -d /path/to/your/directory
```

### Using a PDF for Context

To provide additional context from a PDF file, use the `--pdf` or `-p` flag followed by the file path:

```sh
npx gen-ai-chat "Your question here" --pdf /path/to/your/file.pdf
```

### Interactive Mode

To start the tool in interactive mode, where you can ask multiple questions in a session:

```sh
npx gen-ai-chat -i
```

or

```sh
npx gen-ai-chat --interactive
```

In interactive mode, the prompt `gen-ai-chat>` will appear, indicating that the tool is ready for you to type your question or command.

To exit interactive mode, type `exit` or `quit` and press Enter.

### Choosing Your Favorite Model

You can choose your favorite model interactively by using the `--choose-model` option:

```sh
npx gen-ai-chat --choose-model
```

This command will prompt you to select a model from the available options:

```
? Please select a model: (Use arrow keys)
❯ gemini-pro
  gemini-1.5-flash-latest
  gemini-1.5-pro-latest
  gemini-pro-vision
  text-embedding-004
```

Alternatively, you can specify the model directly using the `--model` option followed by the model name:

```sh
npx gen-ai-chat "Your question here" --model gemini-1.5-flash-latest
```

### Writing Logs to File

By default, logs are stored in memory. To write the in-memory logs to a file, use the `--write-logs` option:

```sh
npx gen-ai-chat --write-logs
```

## Environment Variables

You can provide your own API key by setting the `API_KEY` environment variable in a `.env` file:

```env
API_KEY=your_google_gemini_api_key
```
