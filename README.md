# Multi-modal-early-fusion-transformer

## Horse Lameness Detection Using Transformer and YOLOPose

## Overview

This project aims to detect lameness in horses by leveraging deep learning models. It combines a pre-trained YOLOPose model for keypoint detection and a ResNet50 model for feature extraction from video frames. The extracted features and keypoints are processed through a Transformer model to classify horses as sound or lame.

## Table of Contents

- [Project Structure](#project-structure)
- [Setup and Installation](#setup-and-installation)
- [Usage](#usage)
- [Model Training](#model-training)
- [Inference](#inference)
- [Results](#results)
- [Contributing](#contributing)
- [License](#license)

## Project Structure

```
.
├── data
│   ├── raw
│   ├── processed
│   └── annotations
├── models
│   ├── yolo_pose
│   └── resnet50
├── notebooks
│   └── exploratory_data_analysis.ipynb
├── scripts
│   ├── train.py
│   └── inference.py
├── utils
│   ├── data_processing.py
│   └── visualization.py
├── README.md
└── requirements.txt
```

## Setup and Installation

1. Clone the repository:
    ```sh
    git clone https://github.com/ThuyPh-am/horse-lameness-detection.git
    cd horse-lameness-detection
    ```

2. Install the required packages:
    ```sh
    pip install -r requirements.txt
    ```

3. (Optional) Set up a virtual environment:
    ```sh
    python -m venv venv
    source venv/bin/activate  # On Windows use `venv\Scripts\activate`
    pip install -r requirements.txt
    ```

## Usage

### Data Preparation

- Place your raw videos and annotations in the `data/raw` directory.
- Use the `notebooks/exploratory_data_analysis.ipynb` notebook to explore and preprocess your data.

### Training

To train the Transformer model for horse lameness detection, run:
```sh
python scripts/train.py --config configs/train_config.yaml
```

### Inference

To run inference on a video, use the `inference.py` script:
```sh
python scripts/inference.py --video_path data/raw/test_video.mp4 --model_path models/transformer_model.pth
```

### Configuration

- Adjust the configuration parameters in `configs/train_config.yaml` as needed.

## Results

The results of the model can be visualized as follows:

1. **Visualization of Keypoints**:
    ![Keypoints Example](results/keypoints_example.png)

2. **Model Performance**:
  
## Contributing

Contributions are welcome! Please follow these steps to contribute:

1. Fork the repository.
2. Create a new branch (`git checkout -b feature/your-feature`).
3. Commit your changes (`git commit -am 'Add some feature'`).
4. Push to the branch (`git push origin feature/your-feature`).
5. Create a new Pull Request.

## Contact

For any questions or suggestions, feel free to open an issue or contact the project maintainers.

