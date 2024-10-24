
# Pagination Project 📚

Welcome to the Pagination Project! This repository showcases various methods to efficiently paginate datasets, especially focusing on a CSV file containing popular baby names. Let's dive into the different tasks and functionalities implemented here! 🚀

## Table of Contents

- [Introduction](#introduction)
- [Tasks Overview](#tasks-overview)
  - [0. Simple Helper Function](#0-simple-helper-function)
  - [1. Simple Pagination](#1-simple-pagination)
  - [2. Hypermedia Pagination](#2-hypermedia-pagination)
  - [3. Deletion-Resilient Hypermedia Pagination](#3-deletion-resilient-hypermedia-pagination)
- [Requirements](#requirements)
- [Usage](#usage)
- [Contributions](#contributions)

## Introduction

In this project, we explore how to paginate datasets effectively using Python. We implement basic pagination techniques and enhance them with hypermedia features to create a user-friendly API experience. Plus, we ensure resilience against data deletions! 🌟

## Tasks Overview

### 0. Simple Helper Function

We created a function called `index_range` that calculates the start and end indices for pagination based on the given page and page size. 

```python
def index_range(page: int, page_size: int) -> tuple:
    ...
```

### 1. Simple Pagination

Building on the previous task, we implemented the Server class which loads the baby names dataset and provides a method get_page to retrieve specific pages.

```python
class Server:
    ...
    def get_page(self, page: int = 1, page_size: int = 10) -> List[List]:
        ...
```

### 2. Hypermedia Pagination

We enhanced the Server class with a get_hyper method, returning a dictionary that includes pagination details, such as current page, next page, and total pages.

```python
def get_hyper(self, page: int = 1, page_size: int = 10) -> Dict:
    ...
```

### 3. Deletion-Resilient Hypermedia Pagination

In our final task, we introduced a get_hyper_index method that maintains pagination even if entries are deleted from the dataset, ensuring a smooth user experience.

```python
def get_hyper_index(self, index: int = None, page_size: int = 10) -> Dict:
    ...
```

## Requirements

- Python 3.7
- Files must end with a newline character.
- All files should begin with `#!/usr/bin/env python3`.
- Follow PEP 8 style guidelines (using pycodestyle).
- Include comprehensive documentation for modules and functions.
- Ensure type annotations for all functions and coroutines.

## Usage

Clone the repository:

```bash
git clone https://github.com/yourusername/alx-backend.git
cd 0x00-pagination
```

Run the examples to see the pagination in action:

```bash
python3 0-main.py
python3 1-main.py
python3 2-main.py
python3 3-main.py
```

## Contributions

Contributions are welcome! Feel free to open issues or submit pull requests. Let's enhance this pagination project together! 🤝
