## README.md for Python Web Application

# Overview
This repository contains a Python web application built using the Flask framework. The application displays the current time in Moscow and is structured following best practices in web development.

# Installation
To run the application locally, follow these steps:

1. Clone this repository to your local machine.
2. Navigate to the `app_python` directory.
3. Activate the virtual environment using the command:
   ```bash
   source venv/bin/activate  # For macOS/Linux
   ```
4. Install the required dependencies using:
   ```bash
   pip install -r requirements.txt
   ```
5. Run the Flask application using:
   ```bash
   python app.py
   ```
6. Access the application in your web browser at http://127.0.0.1:5000/.

# Project Structure
- `app.py`: Main application file containing routes and configurations.
- `templates/`: Directory containing HTML templates for rendering views.
- `static/`: Directory for static files such as CSS, JavaScript, and images.

# Dependencies
- Flask
- Jinja2
- Werkzeug

# Testing
To run the unit tests, use the following command:
```bash
python -m unittest discover tests
```

## Docker

### Containerized Application

Our application is containerized using Docker to ensure consistency and portability across different environments. It is based on a lightweight Python image and uses Gunicorn as the WSGI HTTP server.

### How to Use Docker

#### Building the Docker Image

To build the Docker image locally, run the following command in the terminal:

```bash
docker build -t my-python-app .
docker pull your-dockerhub-username/my-python-app:tag
docker run -d --name my-container your-dockerhub-username/my-python-app:tag
```

#CI Workflow

This repository is integrated with GitHub Actions to automate the build and test process. The CI workflow includes the following steps:

**Dependencies:** Install Python dependencies required for the application.
**Linter:** Check the code for linting errors using Flake8.
**Tests:** Run unit tests to ensure code quality and functionality.
**Docker Build & Push:** Build a Docker image of the application and push it to Docker Hub.

## Visit Count

1. **Access the /visits Endpoint:**
   - Send a GET request to the /visits endpoint of your Flask application.
   - For example, if your application is running locally, you can access http://localhost:5001/visits in your web browser or use a tool like cURL or Postman.

2. **Review JSON Response:**
   - Upon accessing the /visits endpoint, your Flask application will respond with a JSON object containing the visit count.
   - Example JSON response: `{"visits": 4.0}`

3. **Confirm Value in visits.txt:**
   - The value provided in the JSON response (e.g., "4.0") should match the content of your visits.txt file.
   - Open the visits.txt file in a text editor or use terminal commands to view its contents.
   - Example content of visits.txt: `4.0`

4. **Verification:**
   - If the value in the JSON response matches the content of visits.txt, it confirms that your Flask application is correctly updating and persisting the visit count in the visits.txt file.
   - This ensures that the visit count is maintained across application restarts and reflects the actual number of visits to your application.


# Contribution
Contributions are welcome! If you find any bugs or have suggestions for improvements, please open an issue or submit a pull request.

# License
This project is licensed under the MIT License - see the LICENSE file for details.

---

