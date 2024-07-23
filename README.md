# Python CI/CD with GitHub Actions and pytest
This repository contains a simple Python application integrated with a CI/CD pipeline using GitHub Actions. The pipeline automatically runs tests using `pytest` on every pull request to ensure code quality and correctness.


## Description of Files

`.github/workflows/ci.yml`: This file configures the GitHub Actions workflow. It sets up the CI/CD pipeline to run on every pull request to the main branch. The workflow includes steps to:

1. Check out the repository code
2. Set up Python (with versions 3.8, 3.9, and 3.10)
3. Install dependencies from requirements.txt
4. Run tests using pytest

- `app/init.py`: Marks the app directory as a Python package.

- `app/main.py`: Contains the main application code with basic arithmetic functions (add and subtract).

- `tests/init.py` : Marks the tests directory as a Python package.

- `tests/test_main.py` : Contains unit tests for the functions defined in app/main.py using pytest.

- `requirements.txt` : Lists the project dependencies, including pytest for testing.

- `README.md` : Provides an overview of the project, repository structure, and instructions for running the application and tests.

## Getting Started

### Prerequisites
Ensure you have the following installed on your local machine:

- **Python 3.8 or higher**
- **pip (Python package installer)**
- **Installation**
- **Clone the repository**:

```sh
git clone https://github.com/yourusername/github-actions-pytest.git
cd github-actions-pytest
```
Install the dependencies:
```sh
pip install -r requirements.txt
```
### Running the Application
You can run the main application code directly. For example, to use the add and subtract functions:

```sh
from app.main import add, subtract

print(add(3, 5))    # Output: 8
print(subtract(10, 5))  # Output: 5
```
### Running Tests
To run the tests using pytest, execute the following command:

```sh
pytest
```

This will automatically discover and run all tests in the tests directory.

## CI/CD Pipeline

The CI/CD pipeline is configured using GitHub Actions in the .github/workflows/ci.yml file. The pipeline runs on every pull request to the main branch and includes the following steps:

- **Checkout**: Retrieves the latest code from the repository.
- **Set up Python**: Sets up the specified versions of Python.
- **Install dependencies**: Installs the required dependencies listed in requirements.txt.
- **Run tests**: Executes the tests using pytest.

**Viewing CI/CD Results** 
After creating a pull request, you can view the status of the CI/CD pipeline in the "Actions" tab of your GitHub repository. Detailed logs and results of the workflow runs will be available there.

## License
This project is licensed under the MIT License. See the LICENSE file for details.
