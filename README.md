# Superhero Recognition from T-Shirts

## Project Overview

This project involves creating a machine learning model that can recognize superhero names from images printed on T-shirts. The technology developed can be used for the automatic classification of products in e-commerce businesses, enhancing the efficiency of inventory management and product search.

## Project Structure

- **super_hero_recognition.py**: The main script containing the code for data preprocessing, model training, and prediction.
- **CAX_Superhero_Train**: Directory containing training images.
- **CAX_Superhero_Test**: Directory containing testing images.
- **train_data.npy**: Numpy array file for storing training data.
- **test_data.npy**: Numpy array file for storing testing data.
- **label.pickle**: Pickle file for storing label dictionary.
- **filename.pickle**: Pickle file for storing test filenames.
- **train_model.h**: Saved weights of the trained model.
- **q4_python.csv**: Output file with predictions.

## Requirements

- Python 3.x
- TensorFlow
- Keras
- OpenCV
- NumPy
- Pandas

Install the required packages using the following command:

\```bash
pip install tensorflow keras opencv-python numpy pandas
\```

## Usage

### 1. Data Preparation

The script assumes the presence of two directories, `CAX_Superhero_Train` and `CAX_Superhero_Test`, containing the training and testing images, respectively. Images should be in `.jpg`, `.png`, or `.jpeg` formats.

### 2. Training the Model

The `create_training_data()` function processes the training images and saves them as numpy arrays. Similarly, `create_testing_data()` processes the test images. The training and validation data are then used to train the convolutional neural network (CNN) model.

\```python
data = create_training_data()
test_data = create_testing_data()
t_model = train_model()
\```

### 3. Making Predictions

After training, the model can be used to predict superhero names from test images. The `prediction()` function loads the test data and model weights, performs predictions, and saves the results in `q4_python.csv`.

\```python
prediction(t_model)
\```

### 4. Output

The predictions are saved in `q4_python.csv`, with columns indicating the filename and the predicted superhero name.

## Contributing

Contributions are welcome! Please fork the repository and create a pull request with your changes.

## License

This project is licensed under the MIT License. See the `LICENSE` file for details.
