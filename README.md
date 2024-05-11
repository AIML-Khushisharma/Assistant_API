# Assistant_API
# Django Backend Application for Assistant Management

This Django application provides CRUD APIs for managing assistant records. Below are instructions for running the application locally and interacting with the API endpoints using Postman.

## Setup and Installation

### Prerequisites
- Python 3.x installed on your system
- Django framework installed (`pip install django`)
- MySQL database server installed and running
- Postman desktop application or web browser extension installed

### Installation Steps
1. Clone the repository:
  git clone <repository-url>
  cd <repository-name>
Replace `<repository-url>` with the URL of your GitHub repository.

2. Install Python dependencies:
  pip install -r requirements.txt

3. Configure the database:
- Create a MySQL database named `assistants`.
- Update the database configuration in `settings.py` to connect to your MySQL server:
  ```python
  DATABASES = {
      'default': {
          'ENGINE': 'django.db.backends.mysql',
          'NAME': 'assistants',
          'USER': 'your_username',
          'PASSWORD': 'your_password',
          'HOST': 'localhost',
          'PORT': '3306',
      }
  }
  ```
  Replace `your_username` and `your_password` with your MySQL credentials.

4. Apply database migrations:
  python manage.py migrate

5. Run the development server:
  python manage.py runserver

6. Your Django application should now be running locally. You can access it at `http://localhost:8000`.

## Interacting with API Endpoints using Postman

### Import Postman Collection
1. Open Postman.
2. Click on the "Import" button in the top-left corner.
3. Select the provided Postman collection JSON file (`assistant_management.postman_collection.json`).
4. The collection should now be imported into Postman.

### Using API Endpoints
1. **List All Assistants (GET):**
- Send a GET request to `http://localhost:8000/assistants/` to retrieve a list of all assistants.

2. **Retrieve Assistant Details (GET):**
- Send a GET request to `http://localhost:8000/assistants/<assistant_id>/` to retrieve details of a specific assistant. Replace `<assistant_id>` with the ID of the assistant.

3. **Create New Assistant (POST):**
- Send a POST request to `http://localhost:8000/assistants/` with the required assistant details in the request body to create a new assistant record.

4. **Update Assistant Details (PUT):**
- Send a PUT request to `http://localhost:8000/assistants/<assistant_id>/` with the updated assistant details in the request body to update an existing assistant record. Replace `<assistant_id>` with the ID of the assistant.

5. **Delete Assistant Record (DELETE):**
- Send a DELETE request to `http://localhost:8000/assistants/<assistant_id>/` to delete a specific assistant record. Replace `<assistant_id>` with the ID of the assistant.

### Error Handling
- The API endpoints handle error cases such as invalid requests or non-existent resources and return appropriate status codes and error messages.

## Contributing
Contributions are welcome! If you encounter any issues or have suggestions for improvement, please feel free to open an issue or submit a pull request.
