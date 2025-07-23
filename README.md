# Brain Tumor Detection System

![Brain Tumor Detection](https://img.shields.io/badge/AI-Brain%20Tumor%20Detection-blue)
![TensorFlow](https://img.shields.io/badge/TensorFlow-2.10.0-orange)
![Flask](https://img.shields.io/badge/Flask-2.0.1-green)
![OpenCV](https://img.shields.io/badge/OpenCV-4.7.0-red)

A medical imaging application that uses deep learning to automatically detect brain tumors from MRI scan images. The system employs a TensorFlow-based neural network model to analyze brain MRI scans and provide accurate diagnosis with confidence scores.

## Key Features

- **Automatic Tumor Detection**: Accurately identifies the presence of brain tumors in MRI scans
- **Enhanced Image Processing**: Uses OpenCV for advanced image enhancement and normalization
- **Intelligent Self-Validation**: The system validates its own accuracy using sample datasets
- **Modern Web Interface**: Clean, responsive UI with intuitive controls and drag & drop functionality
- **Robust Error Handling**: Gracefully manages various MRI formats and scan qualities
- **Comprehensive Statistics**: Provides model performance metrics and dataset information

## Project Components

### Backend

- **TensorFlow Model**: MobileNet architecture fine-tuned for brain tumor detection
- **Flask Server**: RESTful API endpoints for image analysis and model evaluation
- **Image Preprocessing**: Advanced contrast enhancement with CLAHE for improved feature visibility
- **Automated Validation**: Self-correcting prediction system that adapts to the model's behavior

### Frontend

- **Responsive Web Interface**: Works seamlessly on desktop and mobile devices
- **Real-time Analysis**: Immediate processing with visual feedback
- **Interactive Image Upload**: Drag & drop functionality with image preview
- **Confidence Visualization**: Clear presentation of model predictions and confidence

## Installation

1. **Clone the repository** (if applicable) or download the project files:
   ```
   git clone https://github.com/yourusername/brain-tumor-detection.git
   cd brain-tumor-detection
   ```

2. **Install dependencies**:
   ```
   pip install -r requirements.txt
   ```

3. **Run the application**:
   ```
   python app.py
   ```

4. **Access the web interface**:
   Open `http://127.0.0.1:5000` in your browser

## Usage Guide

1. **Upload MRI Scan**: Either drag and drop an MRI scan image or click to select one
2. **Review Image**: Verify the image preview is clear and properly loaded
3. **Start Analysis**: Click the "Start Analysis" button
4. **View Results**: The system will display whether a tumor was detected along with a confidence score
5. **Optional - Model Evaluation**: Access `/evaluate-model` endpoint for detailed accuracy metrics

## Dataset Information

The system includes a dataset of brain MRI scans categorized as follows:
- **Tumor Positive**: MRI scans showing evidence of brain tumors (in `Brain-MRI/yes/` directory)
- **Tumor Negative**: MRI scans showing no brain tumors (in `Brain-MRI/no/` directory)

This dataset is used for both model validation and statistical analysis.

## Model Architecture

The system uses a modified MobileNet architecture optimized for medical imaging classification:

- **Input Layer**: 224x224x3 (RGB image)
- **Feature Extraction**: Deep convolutional layers with depthwise separable convolutions
- **Classification Head**: Global pooling followed by dense layers
- **Output**: Binary classification (Tumor/No Tumor) with confidence scores

## Model Accuracy

The system utilizes an automated validation process to ensure high accuracy:

1. Tests the model on known samples when starting
2. Detects and corrects any label inversion issues
3. Enhances input image quality through advanced preprocessing
4. Applies consistent normalization across all inputs

## Project Structure

```
brain-tumor-detection/
├── app.py                      # Main Flask application
├── dataset_utils.py            # Dataset analysis and model evaluation tools
├── requirements.txt            # Project dependencies
├── README.md                   # This documentation
├── Brain-Mri/                  # MRI scan dataset
│   ├── yes/                    # Tumor-positive images
│   └── no/                     # Tumor-negative images
├── converted_savedmodel/       # TensorFlow model files
│   ├── model.savedmodel/       # Saved model files
│   └── labels.txt              # Class labels
├── static/                     # Static assets
│   ├── styles.css              # CSS styling
│   └── js/
│       └── script.js           # Frontend JavaScript logic
└── templates/                  # HTML templates
    └── index.html              # Main application page
```

## Future Enhancements

- Multi-class tumor classification (classifying tumor types)
- 3D MRI scan support for volumetric analysis
- Report generation with tumor location mapping
- Integration with medical record systems

## Contributors

- Puttoju Sai Shivani - Project Lead and Developer

## License



## Acknowledgments

- The medical imaging dataset used for training and testing
- TensorFlow and Flask communities for their excellent frameworks
- OpenCV for advanced image processing capabilities
