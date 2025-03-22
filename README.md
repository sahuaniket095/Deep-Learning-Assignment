# FastAPI Prediction Server

This project provides a FastAPI server to serve predictions from trained models.

## Setup Environment

1. **Clone the repository:**
    ```sh
    git clone <repository-url>
    cd <repository-directory>
    ```

2. **Create a virtual environment:**
    ```sh
    python -m venv venv
    ```

3. **Activate the virtual environment:**
    - On Windows:
        ```sh
        venv\Scripts\activate
        ```
    - On macOS/Linux:
        ```sh
        source venv/bin/activate
        ```

4. **Install the required dependencies:**
    ```sh
    pip install -r requirements.txt
    ```

## Running the FastAPI Server

1. **Ensure you have `uvicorn` installed:**
    ```sh
    pip install uvicorn
    ```

2. **Run the server:**
    ```sh
    uvicorn app:app --reload
    ```

3. **Access the server:**
    Open your browser and navigate to `http://127.0.0.1:8000`.

## Testing the API

### Home Endpoint

- **URL:** `http://127.0.0.1:8000/`
- **Method:** `GET`
- **Response:**
    ```json
    {
        "message": "Welcome to the FastAPI Prediction Server"
    }
    ```

### List Models Endpoint

- **URL:** `http://127.0.0.1:8000/models`
- **Method:** `GET`
- **Response:**
    ```json
    {
        "models": ["NN"]
    }
    ```

### Predict Endpoint

- **URL:** `http://127.0.0.1:8000/predict/NN`
- **Method:** `POST`
- **Request Body:**
    ```json
    {
        "features": [0.5, 1.2, 3.3, 4.4, 5.5, 6.6, 7.7, 8.8, 9.9, 10.1, 11.2]
    }
    ```
- **Response:**
    ```json
    {
        "prediction": [result]
    }
    ```

