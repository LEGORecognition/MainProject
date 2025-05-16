# Lego Pieces Recognition Model

This repository contains Lego pieces recognition model trained on pretrained YOLO v11.

Yolo v11: [https://docs.ultralytics.com/models/yolo11/](https://docs.ultralytics.com/models/yolo11/)
Dataset: [https://www.kaggle.com/datasets/ronanpickell/b100-lego-detection-dataset](https://www.kaggle.com/datasets/ronanpickell/b100-lego-detection-dataset)

## The idea

Yolo used to detect 200 classes.

CNN to detect 40 colors.

## Training the model

Create python venv:

```terminal
python -m venv .venv
```

Activate it:

```terminal
# Windows
.\.venv\Scripts\activate.bat
# Linux / MacOs
source .venv/bin/activate
```

Install dependencies:

```terminal
pip install ultralytics --no-deps ipykernel numpy matplotlib pandas pyyaml pillow psutil requests tqdm scipy seaborn ultralytics-thop torch torchvision --upgrade --force-reinstall --index-url https://download.pytorch.org/whl/cu118 opencv-python-headless
```

Open [`lego_ai.ipynb`](./lego_ai.ipynb) and run all cells.
