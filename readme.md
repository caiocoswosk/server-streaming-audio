# Audio Streaming Server in Node.js

This project is a simple audio streaming server built with Node.js, developed as part of the **Computer Graphics and Digital Media** course at Universidade Federal do Espírito Santo. The server streams audio files (e.g., MP3) over HTTP, supporting partial content requests (range requests) for efficient playback and seeking. It also includes an `index.html` file for easy testing and demonstration.

## Features

- **Streaming Support**: Streams audio files in chunks using HTTP range requests.
- **Partial Content Handling**: Allows clients to seek within the audio file.
- **Web Interface**: Includes an `index.html` file with an HTML5 audio player for testing.
- **Lightweight**: Built with Node.js core modules (`http`, `fs`, and `path`).

## How It Works

The server reads an audio file (e.g., `sample.mp3`) and streams it to the client. If the client supports range requests (e.g., browsers or media players), the server responds with the appropriate chunk of the file, enabling features like seeking and pause/resume. The `index.html` file provides a simple web interface to test the streaming functionality.

## Project Structure

- **`server.js`**: The main Node.js server script.
- **`index.html`**: A simple HTML file with an embedded audio player for testing.
- **`sample.mp3`**: An example audio file for streaming (replace with your own file).

## Usage

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/audio-streaming-server.git
   ```
2. Install dependencies (if any):
   ```bash
   npm install
   ```
3. Start the server:
   ```bash
   node server.js
   ```
4. Open your browser and navigate to `http://localhost:3000` to access the `index.html` page with the audio player.

## Example

The `index.html` file contains an HTML5 audio player that connects to the streaming server:

```html
<audio controls>
  <source src="http://localhost:3000/sample.mp3" type="audio/mpeg" />
  Your browser does not support the audio element.
</audio>
```

## Project Context

This project was developed as part of the **Computer Graphics and Digital Media** course, focusing on practical applications of media streaming and server-side technologies. It demonstrates key concepts such as:

- HTTP protocol and range requests.
- Streaming media for efficient playback.
- Integration of web interfaces with backend servers.
