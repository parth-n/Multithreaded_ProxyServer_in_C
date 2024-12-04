# Multi-threaded Proxy Server with Caching

## Overview

This project implements a multi-threaded proxy server in C that efficiently handles multiple client requests concurrently. The server includes a caching mechanism to store and retrieve HTTP responses, significantly improving response times for repeated requests. The project also integrates the `uthash` library to optimize search operations within the cache.

## Features

- **Multi-threaded Handling**: Utilizes POSIX threads to manage multiple client connections simultaneously.
- **Optimized Caching**: Implements a hash map using the `uthash` library for O(1) average time complexity in cache lookups.
- **Thread Safety**: Ensures robust synchronization and error handling with mutex locks and semaphores.
- **LRU Cache Eviction**: Implements a Least Recently Used (LRU) policy to manage cache size and evict old entries.

## Project Structure

- `proxy_server_with_cache.c`: Main source file containing the implementation of the proxy server and caching mechanism.
- `proxy_parse.c` and `proxy_parse.h`: Helper files for parsing HTTP requests.
- `uthash.h`: Header-only library for hash map implementation.
- `Makefile`: Build script for compiling the project.

## Getting Started

### Prerequisites

- GCC compiler
- POSIX-compliant operating system (e.g., Linux, macOS)
- `uthash` library (included in the project)

### Building the Project

To compile the project, run the following command:

```sh 
make


./proxy <port_number>