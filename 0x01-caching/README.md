
# Redis Caching and Tracking Project

## Overview
This project demonstrates basic caching and tracking of web requests using Redis with Python on Ubuntu 18.04 LTS. It utilizes the Redis `get_page` function for request caching and tracking and focuses on efficient use of caching for repeated requests to the same URL.

## Features
- **Caching of Web Requests**: Caches the contents of pages accessed through URLs.
- **Tracking URL Access Frequency**: Records the number of times each URL is accessed.
- **Efficient Performance**: Uses Redis as a simple, fast, in-memory data structure store to optimize repeated requests.

## Requirements
- **Python 3.7**
- **Redis Server** installed on Ubuntu 18.04 LTS
- **Python Packages**: `redis`, `requests`
- **Coding Style**: Follows `pycodestyle` (version 2.5) standards with type annotations and documentation.

## Installation

1. **Install Redis**:
    ```bash
    sudo apt update
    sudo apt install redis-server
    ```

2. **Set up Python Environment**:
    ```bash
    sudo apt install python3-pip
    pip3 install redis requests pycodestyle
    ```

3. **Start Redis Server**:
    ```bash
    sudo service redis-server start
    ```

## Usage

1. **Clone the Repository**:
    ```bash
    git clone https://github.com/your_username/alx-backend-storage.git
    cd alx-backend-storage/0x02-redis_basic
    ```

2. **Run the `get_page` function**:
    ```python
    from your_module import get_page
    get_page("http://example.com")
    ```

3. **View Access Counts**:
   Use Redis commands to check the URL access counts in the Redis CLI:
    ```bash
    redis-cli
    GET "count:http://example.com"
    ```


