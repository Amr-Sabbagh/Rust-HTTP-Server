# Rust TCP-HTTP Server
This is project is part of my Rust learning journey by implementing a simple TCP web server using Rust. A simple, single-threaded TCP-based HTTP server written in Rust. This server binds to the local address `http://127.0.0.1:7878` and handles HTTP requests.

## Features

- Listens on `http://127.0.0.1:7878`
- Responds to `GET` requests on `/` with `200 OK` and a corresponding HTML page
- Responds to any other requests or endpoints with `404 NOT HERE` and an appropriate HTML page

## Getting Started

### Prerequisites

- Rust (latest stable version) installed on your machine.

If Rust is not installed, follow the instructions at: [https://www.rust-lang.org/tools/install](https://www.rust-lang.org/tools/install)

### Cloning the Repository

```bash
git clone https://github.com/Amr-Sabbagh/Rust-HTTP-Server.git
cd Rust-HTTP-Server
```

### Running the Server

To run the server, use the following command:

```bash
cargo run
```

The server will start and bind to `127.0.0.1:7878`.

### Example Usage

1. Open a browser or use a tool like `curl` to test the server:

#### GET Request on `/`

```bash
curl http://127.0.0.1:7878/
```
**Response:**
```
HTTP/1.1 200 OK
Content-Type: text/html

<HTML content>
```

#### Any Other Request

```bash
curl http://127.0.0.1:7878/other
```
**Response:**
```
HTTP/1.1 404 NOT HERE
Content-Type: text/html

<HTML content>
```

## Project Structure

- `src/main.rs`: Contains the main logic for the server, including request handling.
- `templates/`: Contains example HTML files for responses.

## Future Improvements

- Add multithreading for better concurrency.
- Improve error handling and logging.
