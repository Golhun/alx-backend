# i18n with Flask-Babel

## Overview

This project focuses on internationalization (i18n) in Flask, a micro web framework for Python. The goal is to learn how to parameterize Flask templates to display different languages, infer the correct locale based on URL parameters, user settings, or request headers, and localize timestamps.

## Learning Objectives

- **Parametrize Flask templates**: Learn to display different languages using Flask-Babel.
- **Locale inference**: Infer the correct locale from URL parameters, user settings, or request headers.
- **Timestamp localization**: Localize timestamps based on the inferred locale.

## Requirements

- **Python Version**: All files are interpreted/compiled on Ubuntu 18.04 LTS using Python 3.7.
- **Code Style**: Adhere to pycodestyle (version 2.5).
- **File Structure**: All files should end with a new line.
- **Execution**: The first line of all Python files should be `#!/usr/bin/env python3` and should be executable.
- **Documentation**:
  - Modules, classes, functions, and methods must have proper documentation.
  - Documentation should be in full sentences explaining the purpose.
  - All functions and coroutines must be type-annotated.

## Resources

- [Flask-Babel Documentation](https://pythonhosted.org/Flask-Babel/)
- [Flask i18n tutorial](https://blog.miguelgrinberg.com/post/the-flask-mega-tutorial-part-xiii-i18n-and-l10n)
- [pytz Documentation](https://pythonhosted.org/pytz/)

## Installation

To install the required packages, use the following command:

```bash
pip install Flask-Babel pytz
```

## Usage

1. **Initialization**: Import Flask-Babel and initialize it in your Flask app.
2. **Setting Up Languages**: Configure the languages you want to support in your Flask app.
3. **Locale Inference**: Implement functions to infer the locale from URL parameters, user settings, or request headers.
4. **Localization**: Use Flask-Babel to localize timestamps and text.

## Example

```python
from flask import Flask, request
from flask_babel import Babel

app = Flask(__name__)
babel = Babel(app)

@babel.localeselector
def get_locale():
    return request.accept_languages.best_match(['en', 'es', 'fr'])

@app.route('/')
def home():
    return "Hello, World!"

if __name__ == "__main__":
    app.run()
```

## Conclusion

This project is an introduction to internationalization in Flask, focusing on practical implementation using Flask-Babel. Following the learning objectives will equip you with the skills to create multi-language Flask applications.
