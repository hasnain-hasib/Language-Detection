# Language Prediction API

This is a FastAPI web application that provides an API for predicting the language of input text.

## Features

- Endpoint to predict the language of a given text.
- Endpoint to check the health of the application and retrieve the current version of the machine learning model.
- Efficient language prediction using a pre-trained machine learning model.
- Preprocessing of input text to improve prediction accuracy.

## Tech Stack

- **Python**: The main programming language used for the application.
- **FastAPI**: A modern, fast (high-performance), web framework for building APIs with Python.
- **Pydantic**: A data validation and settings management library, used for defining the input and output data models.
- **Pickle**: A Python module used for serializing and deserializing Python objects, used to load the pre-trained machine learning model.

## Installation

1. Clone the repository:
```
git clone https://github.com/your-username/language-prediction-api.git
```

2. Change to the project directory:
```
cd language-prediction-api
```

3. Create a virtual environment and activate it:
```
python -m venv venv
source venv/bin/activate  # On Windows, use `venv\Scripts\activate`
```

4. Install the required dependencies:
```
pip install -r requirements.txt
```

## Usage

1. Start the FastAPI server:
```
uvicorn app.main:app --reload
```

2. The API will be available at `http://localhost:8000`.

3. You can use the `/predict` endpoint to send a POST request with a JSON payload containing the text to be predicted, and it will return the predicted language.

Example request:
```
curl -X POST -H "Content-Type: application/json" -d '{"text": "This is an example text."}' http://localhost:8000/predict
```

Example response:
```
{
    "language": "English"
}
```

4. The `/` endpoint can be used to check the health of the application and retrieve the current version of the machine learning model.

## Deployment

The application can be deployed on various platforms, such as Heroku, AWS, or Docker. The deployment process will depend on the chosen platform and the specific requirements of your project.

## Contributing

If you find any issues or have suggestions for improvements, feel free to open an issue or submit a pull request.

## License

This project is licensed under the [MIT License](LICENSE).
