# Apple and Banana Detection Project

This project uses YOLOv5 to detect apples and bananas in images. The dataset is sourced from [Kaggle](https://www.kaggle.com/datasets/shreyapmaher/fruits-dataset-images), and annotations were done using Roboflow.

## Project Structure

apple-banana-detection/
¢u¢w¢w README.md
¢u¢w¢w .gitignore
¢u¢w¢w apple_banana_detection.ipynb
¢u¢w¢w train.py
¢u¢w¢w test.py
¢u¢w¢w preprocess.py
¢u¢w¢w data/
¢x ¢u¢w¢w images/
¢x ¢u¢w¢w labels/
¢u¢w¢w models/
¢x ¢|¢w¢w best.pt
¢|¢w¢w config/
¢|¢w¢w yolov5s.yaml


## Installation

1. Clone this repository:
    ```bash
    git clone https://github.com/yourusername/apple-banana-detection.git
    cd apple-banana-detection
    ```

2. Install dependencies:
    ```bash
    pip install -r requirements.txt
    ```

3. Download the dataset and unzip it into `data/images` directory:
    You can download the dataset from [Kaggle](https://www.kaggle.com/datasets/shreyapmaher/fruits-dataset-images) and manually unzip it, or use Kaggle API:
    ```bash
    kaggle datasets download -d shreyapmaher/fruits-dataset-images -p data/images
    unzip data/images/fruits-dataset-images.zip -d data/images
    ```

## Usage

1. Preprocess the data (if necessary):
    ```bash
    python preprocess.py
    ```

2. Train the model:
    ```bash
    python train.py --data data.yaml --cfg config/yolov5s.yaml --weights yolov5s.pt --epochs 100
    ```

3. Test the model:
    ```bash
    python test.py --weights models/best.pt --img 640 --conf 0.25 --source data/images/
    ```

## Results Showcase

Here are some examples of the model detecting apples and bananas:
![Example 1](examples/example1.jpg)
![Example 2](examples/example2.jpg)

## Technical Challenges and Solutions

- **Challenge 1**: Describe the first challenge and its solution.
- **Challenge 2**: Describe the second challenge and its solution.

## Reflection and Future Work

- **Reflection**: What did you learn from this project?
- **Future Work**: What are potential extensions or improvements?

## Contribution Guidelines

Contributions are welcome! Please open an issue or submit a pull request.

## Contact

For any questions or suggestions, please contact [Your Name]: [your.email@example.com].