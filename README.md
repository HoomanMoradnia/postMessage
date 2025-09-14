# postMessage

A simple project for demonstrating or experimenting with the `postMessage` API in web development.

## Overview

This repository is intended to showcase how to use the `postMessage` method, which allows for safe cross-origin communication between Window objects in web browsers. It's particularly useful for messaging between an iframe and its parent, or between different browser windows or tabs.

## Features

- Example code using the `postMessage` API.
- Demonstrates sending and receiving messages between documents.
- Can be extended for tutorials, learning, or as boilerplate for messaging in web apps.

## Usage

1. Clone the repository:
   ```sh
   git clone https://github.com/HoomanMoradnia/postMessage.git
   ```
2. Change directory to the project folder:
   ```sh
   cd postMessage
   ```
3. Start a web server (for example, using Python) and open `receiver.html`:
   ```sh
   # Using Python 3.x
   python -m http.server 8000
   ```
   Then, in your browser, go to [http://localhost:8000/receiver.html](http://localhost:8000/receiver.html).

4. Open a different terminal window, start another web server on a different port, and open `sender.html`:
   ```sh
   python -m http.server 9000
   ```
   Then, in your browser, go to [http://localhost:9000/sender.html](http://localhost:9000/sender.html).

5. On the `sender.html` page, click the button to send a message. Observe the result on the popup page.

## How it Works

- The sender document uses `window.postMessage(message, targetOrigin)` to send a message.
- The receiver listens for the `message` event using `window.addEventListener('message', handler)`, and handles the message accordingly.
- The demo ensures only trusted origins are processed for security.

## License

This project is licensed under the [MIT License](LICENSE).

---

*Maintained by [HoomanMoradnia](https://github.com/HoomanMoradnia)*
