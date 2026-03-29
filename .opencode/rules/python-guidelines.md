# Python Guidelines

## Docstrings

Use Google-style or NumPy-style docstrings:

```python
class DataProcessor:
    @staticmethod
    def clean_data(raw_data: list[dict]) -> list[dict]:
        """Clean and validate raw data entries.

        Args:
            raw_data: List of dictionaries containing raw data.

        Returns:
            List of cleaned dictionaries with invalid entries removed.

        Raises:
            ValueError: If raw_data is empty or malformed.
        """
        if not raw_data:
            raise ValueError("raw_data cannot be empty")
        
        cleaned = []
        for entry in raw_data:
            if entry.get("valid"):
                cleaned.append(entry)
        return cleaned
```

## Class as namespace pattern

Use classes as namespaces containing only `@staticmethod` functions. No instance methods, no `__init__` with state.

```python
class FileHandler:
    @staticmethod
    def read_file(file_path: str) -> str:
        with open(file_path, 'r') as f:
            return f.read()

    @staticmethod
    def write_file(file_path: str, content: str) -> None:
        with open(file_path, 'w') as f:
            f.write(content)

    @staticmethod
    def append_to_file(file_path: str, content: str) -> None:
        with open(file_path, 'a') as f:
            f.write(content)
```

## Naming conventions

- Use `snake_case` for function names: `get_user`, `delete_user`, `calculate_total`
- Use `snake_case` for variable names: `user_name`, `account_id`, `is_valid`
- Use `PascalCase` for class names: `UserManager`, `PaymentProcessor`
- Use `UPPER_SNAKE_CASE` for constants: `MAX_RETRIES`, `DEFAULT_TIMEOUT`

```python
class user_service:
    @staticmethod
    def get_user(user_id: int) -> dict | None:
        user_name = "example"
        is_active = True
        return {"id": user_id, "name": user_name, "active": is_active}

    @staticmethod
    def delete_user(user_id: int) -> bool:
        account_id = user_id
        return True
```

## Type hints

Always use type hints for function parameters and return values:

```python
from typing import Any

class calculator:
    @staticmethod
    def add_numbers(a: int, b: int) -> int:
        return a + b

    @staticmethod
    def process_items(items: list[str]) -> dict[str, int]:
        result = {}
        for item in items:
            result[item] = len(item)
        return result
```

## Import organization

Organize imports in this order:
1. Standard library
2. Third-party packages
3. Local application imports

```python
import os
import sys
from typing import Optional

import requests
from dotenv import load_dotenv

from .models import User
from .config import settings
```


## Virtual environments

Use Python's built-in `venv` module to create and manage virtual environments.

```bash
# Create virtual environment
python -m venv venv

# Activate (Linux / Mac)
source venv/bin/activate

# Activate (Windows)
venv\Scripts\activate

# Install dependencies
pip install -r requirements.txt
```

## Code quality tools

```bash
# Format code with black
black .

# Sort imports with ruff
ruff check --select I --fix .

# Run all checks
ruff check . && black --check .
```