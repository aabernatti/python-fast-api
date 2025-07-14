# FastAPI Project

This is a simple FastAPI web application that serves an HTML page using Jinja2 templates. The project is containerized with Docker and includes a CircleCI configuration for continuous integration.

## Features
- FastAPI backend
- Jinja2 templating
- Docker support
- CircleCI for CI/CD

## Project Structure
```
python-fast-api/
├── app/
│   ├── main.py
│   └── templates/
│       └── index.html
├── .circleci/
│   └── config.yml
├── dockerfile
├── requirements.txt
├── .gitignore
└── README.md
```

## Getting Started

### Prerequisites
- Python 3.11+
- pip
- Docker (optional, for containerization)

### Installation
1. Clone the repository:
   ```bash
   git clone <repo-url>
   cd python-fast-api
   ```
2. Install dependencies:
   ```bash
   python -m venv venv
   source venv/bin/activate
   pip install -r requirements.txt
   ```

### Running the App Locally
```bash
uvicorn app.main:app --reload
```
Visit [http://127.0.0.1:8000/index](http://127.0.0.1:8000/index) in your browser.

### Docker Usage
Build and run the Docker container:
```bash
docker build -t python-fast-api .
docker run -p 8003:8003 python-fast-api
```
The app will be available at [http://localhost:8003/index](http://localhost:8003/index).

### CircleCI
The project includes a `.circleci/config.yml` for CI/CD. It installs dependencies, lints the code, and tests server startup.

## API Endpoints
- `/` : Redirects to `/index`
- `/index` : Renders the `index.html` template

## Requirements
- fastapi
- uvicorn[standard]
- jinja2

## License
Specify your license here. 