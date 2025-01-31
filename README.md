# Multithreaded Proxy Web Server with LRU Caching

A high-performance HTTP/HTTPS proxy server implemented in C, supporting concurrent client connections using pthreads and LRU (Least Recently Used) caching for efficient resource management.

## Features
- **Multithreaded Architecture**: Handles multiple clients simultaneously using pthreads.
- **LRU Caching**: Caches frequently accessed resources with configurable size.
- **HTTP/1.1 Support**: Basic HTTP methods (GET, POST) with header parsing.
- **Connection Pooling**: Reusable connections to backend servers.
- **Configurable Settings**: Adjust cache size, port, and concurrency limits.

## Technologies
- **C17 Standard**
- POSIX Threads (`pthread`)
- BSD Sockets API
- LRU Cache Implementation
- Makefile Build System

## Prerequisites
- GCC (GNU Compiler Collection) ≥ 9.0
- GNU Make
- pthread library
- curl (for testing)
- Wireshark/tshark (optional, for network analysis)

## Installation

```bash
# Clone repository
git clone https://github.com/yourusername/proxy-server.git
cd proxy-server

# Build project
make all

# Start proxy server (default port 8080)
./bin/proxy-server
