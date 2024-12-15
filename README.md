# Template Django Sample

This repository provides a sample project to demonstrate best practices and foundational implementations in Django. Ideal for developers looking to understand Django's architecture or as a starting point for new projects.

## Features

- Modular structure following Django's best practices.
- Examples of template rendering and static file usage.
- Preconfigured settings for rapid development.
- Easily extendable for various use cases.

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/shahramsamar/template_Django_sample.git
   ```

2. Navigate to the project directory:
   ```bash
   cd template_Django_sample
   ```

3. Create and activate a virtual environment:
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

4. Install the dependencies:
   ```bash
   pip install -r requirements.txt
   ```

5. Apply database migrations:
   ```bash
   python manage.py migrate
   ```

6. Run the development server:
   ```bash
   python manage.py runserver
   ```

## Usage

1. Access the application at `http://127.0.0.1:8000/`.
2. Modify templates in the `templates/` directory to suit your needs.
3. Add static files (e.g., CSS, JS) in the `static/` directory and reference them in templates.

## Example Code

### Template Example
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Home Page</title>
</head>
<body>
    <h1>Welcome to the Template Django Sample</h1>
    <p>{{ message }}</p>
</body>
</html>
```

### View Example
```python
from django.shortcuts import render

def home(request):
    return render(request, 'home.html', {'message': 'Hello, Django World!'})
```

### URL Configuration
```python
from django.urls import path
from .views import home

urlpatterns = [
    path('', home, name='home'),
]
```

## Requirements

- Python 3.7+
- Django 3.2+

## Contributing

Contributions are welcome! Please follow these steps:

1. Fork the repository.
2. Create a new branch for your feature or bugfix.
3. Commit your changes with clear messages.
4. Push your branch and create a pull request.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for more details.

## Contact

- **Author**: Shahramsamar
- **Email**: [shahramsamar2010@gmail.com](mailto:shahramsamar2010@gmail.com)
- **GitHub**: [Shahramsamar](https://github.com/shahramsamar)

![Alt](https://repobeats.axiom.co/api/embed/eabe6508a91fa38b4ace0060919094363916f544.svg "Repobeats analytics image")
