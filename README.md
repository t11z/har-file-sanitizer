# HAR File Sanitizer

A fast, zero-knowledge, client-side tool to redact sensitive information from `.har` (HTTP Archive) files before sharing them for debugging purposes.

## Features

- **Zero Knowledge / Local Only:** Everything runs entirely in your browser using Vanilla JavaScript. No data is ever uploaded to a server.
- **Single File:** The entire application is contained within a single `index.html` file.
- **Customizable Sanitization:**
  - Redact Auth & Cookie Headers (`Authorization`, `Cookie`, `Set-Cookie`).
  - Redact explicit Cookie objects.
  - Scrub POST payloads (form parameters and raw text).
  - Target sensitive query parameters (`token`, `password`, `secret`, `session`, etc.).

## Usage

1. Open `index.html` in any modern web browser, or host it statically.
2. Drag and drop your exported `.har` file into the dropzone.
3. Select the data you want to redact.
4. Click **Sanitize & Download**. The sanitized file will automatically download as `*_sanitized.har`.

## Security

Because this tool is a single HTML file without external dependencies (except Tailwind CSS via CDN for styling), you can easily inspect the source code to verify that no network requests are made with your data. You can also save the file and run it completely offline.

## License

This project is open-sourced under the MIT License. See the `LICENSE` file for details.
