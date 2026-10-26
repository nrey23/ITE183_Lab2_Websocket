# ITE183 Laboratory 2: WebSocket Server

A real-time WebSocket chat application developed using Bonezegei Scripting Language (BSL) v1.3.3 for ITE183 – Web Systems and Technologies.

## Project Description

This laboratory demonstrates how a WebSocket server enables real-time, full-duplex communication between multiple connected clients. The application allows users to send messages and receive broadcasts without refreshing their browser.

## Features

- HTTP server running on port 8000
- WebSocket client connections and disconnections
- Welcome messages for newly connected clients
- Real-time message broadcasting to all connected clients
- HTML-based chat interface
- Custom page for undefined routes

## Technologies Used

- Bonezegei Scripting Language v1.3.3
- Bonezegei HTTP package
- HTML, CSS, and JavaScript
- WebSocket API
- Visual Studio Code

## Installation and Setup

1. Install Bonezegei Scripting Language v1.3.3.
2. Clone this repository and open the project folder.
3. Open a terminal and run:

   ```bash
   bonezegei -v
   bzg install
   ```

4. On Windows, the HTTP library may require `libwinpthread-1.dll`. If the dependency is missing, obtain the appropriate x64 runtime from the [official MSYS2 package](https://packages.msys2.org/packages/mingw-w64-ucrt-x86_64-libwinpthread), verify the downloaded package checksum against its official publication, and make the DLL available in the application's DLL search path.

5. Start the server:

   ```bash
   bzg run
   ```

6. Open `http://localhost:8000` in a browser.

## Testing

Open the application in two browser windows. Send a message from one window and verify that both windows receive the broadcast. Repeat the process using the second window.

To test the custom error page, navigate to `http://localhost:8000/unknown`.

Note: The current implementation displays the custom 404 page but returns HTTP status 200.

## Project Structure

```text
ITE183_Lab2_Websocket/
├── .gitattributes
├── .gitignore
├── LICENSE
├── README.md
├── package.json
├── app.bzg
└── public/
    ├── index.html
    └── 404.html
```

The `lib/` directory and locally installed native runtime DLL are excluded from Git and are recreated or supplied during local setup.

## Reference

[BSL HTTP and WebSocket – Professor's Sample Repository](https://github.com/msuiit-ph/BSL_HTTP_and_WebSocket)

## License

This project is licensed under the MIT License.