# Server-Sent Events Demo

This project demonstrates the use of Server-Sent Events (SSE) with Node.js and a simple HTML frontend.

## Features
- Node.js backend serving SSE messages
- Simple HTML frontend that connects and displays streamed messages in real time

## Files
- `index.js`: Node.js Express server that serves the HTML file and provides the `/stream` SSE endpoint. Messages are sent every second to connected clients.
- `index.html`: Frontend page that connects to `/stream` using EventSource and displays incoming messages.
- `package.json`: Project metadata and dependencies (uses Express).

## How to Run
1. Install dependencies:
   ```bash
   npm install
   ```
2. Start the server:
   ```bash
   node index.js
   ```
3. Open your browser and navigate to `http://localhost:8080` to view the demo.

## How It Works
- The backend uses Express to serve `index.html` and provide a `/stream` endpoint.
- The `/stream` endpoint uses the `text/event-stream` content type to push messages to the client every second.
- The frontend connects to `/stream` using the `EventSource` API and appends incoming messages to the page.

## License
This project is licensed under the ISC License.
