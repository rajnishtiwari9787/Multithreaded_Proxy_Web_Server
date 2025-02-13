# Multithreaded Proxy Web Server with LRU Caching

A high-performance, multithreaded HTTP/HTTPS proxy server implemented in C, designed to efficiently manage concurrent client connections and optimize resource usage with an LRU (Least Recently Used) caching mechanism.

## Features
- 🚀 **Multithreaded Architecture**: Supports concurrent client connections using POSIX threads (`pthread`).
- 🗂 **LRU Caching**: Implements an efficient Least Recently Used (LRU) caching strategy to store frequently accessed resources, improving response times.
- 🌐 **HTTP/1.1 Support**: Handles essential HTTP methods (`GET`, `POST`) with robust header parsing.
- 🔄 **Connection Pooling**: Reuses backend server connections to optimize performance and reduce latency.
- ⚙️ **Configurable Settings**: Customize cache size, port number, concurrency limits, and other server parameters via configuration.

## Technologies Used
- **C17 Standard**
- **POSIX Threads (`pthread`)**
- **BSD Sockets API**
- **LRU Cache Implementation**
- **Makefile Build System**

## Prerequisites
Ensure your system meets the following requirements before building and running the proxy server:
- GCC (GNU Compiler Collection) ≥ 9.0
- GNU Make
- POSIX `pthread` library
- `curl` (for testing HTTP requests)
- `Wireshark`/`tshark` (optional, for network traffic analysis)

## Installation & Usage

### 1️⃣ Clone the Repository
```bash
git clone https://github.com/rajnishtiwari9787/proxy-server.git
cd proxy-server
```

### 2️⃣ Build the Project
```bash
make all
```

### 3️⃣ Start the Proxy Server
```bash
./bin/proxy-server
```

By default, the proxy runs on **port 8080**. To specify a different port, pass it as an argument:
```bash
./bin/proxy-server <port_number>
```

## Testing the Proxy Server
You can test the proxy functionality using `curl`:
```bash
curl -x http://localhost:8080 http://example.com
```
Or analyze traffic using `Wireshark` or `tshark`:
```bash
tshark -i any -f "tcp port 8080"
```

## Configuration
Modify the **configuration file** (`config.h` or runtime arguments) to adjust:
- Cache size
- Thread pool size
- Logging options
- Timeout settings

## Contribution
Contributions are welcome! Feel free to open issues, submit pull requests, or suggest enhancements.

## License
This project is licensed under the MIT License. See `LICENSE` for details.

---
🛠 **Built with performance and efficiency in mind. Happy coding!**

