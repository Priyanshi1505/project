# project
**Logistic Regression Prediction Flask API**

This Flask application functions as a basic API endpoint (`/get_predictions`) designed to receive user input, utilize a pre-trained logistic regression model for predictions, and furnish the outcome of the model's predictions.
The script loads a pre-trained logistic regression model by employing the `joblib` library, assuming the model is stored in the specified path ('model1/log_reg.joblib').

**API Endpoint Definition:**
--The Flask application defines a singular API endpoint, `/get_predictions`, configured to accept HTTP POST requests. Users can transmit input data as JSON within the request body.
**Processing Predictions:**
--Upon receiving a request, the script extracts the user-supplied data from the JSON payload and transforms it into a NumPy array. This array is then reshaped to conform to the expected input format of the logistic regression model.
**Model Prediction:**
--The logistic regression model predicts the class based on the input data provided by the user.
**Response Handling:**
--The script communicates the model's predictions as a straightforward string within the HTTP response.
**Error Management:**
--The application incorporates elementary error handling to handle exceptions. In case of an error during processing, an error message is returned with a 500 status code, or 404 if it is an internal server error.
**Deployment:**
--Upon execution of the script, the Flask application activates, rendering the API accessible.
