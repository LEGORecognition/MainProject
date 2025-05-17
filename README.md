# LEGO® Bricks Detection

This repository contains LEGO® bricks detection model trained on YOLO. It detects pieces on an image and matches them to their respective piece ID and color ID.

Yolo v11: [https://docs.ultralytics.com/models/yolo11/](https://docs.ultralytics.com/models/yolo11/) \
Dataset: [https://www.kaggle.com/datasets/ronanpickell/b100-lego-detection-dataset](https://www.kaggle.com/datasets/ronanpickell/b100-lego-detection-dataset) \
LEGO® Catalog: [https://www.lego.com/en-us/pick-and-build/pick-a-brick](https://www.lego.com/en-us/pick-and-build/pick-a-brick)

## The idea

Yolo used to detect 200 brick ID classes.

CNN to detect 40 colors.

## Training the model

1. Create python venv:

```terminal
python -m venv .venv
```

2. Activate it:

```terminal
# Windows
.\.venv\Scripts\activate.bat
# Linux / MacOs
source .venv/bin/activate
```

3. Install dependencies:

```terminal
pip install ultralytics --no-deps ipykernel numpy matplotlib pandas pyyaml pillow psutil requests tqdm scipy seaborn ultralytics-thop torch torchvision --upgrade --force-reinstall --index-url https://download.pytorch.org/whl/cu118 opencv-python-headless
```

4. Open [`lego_ai.ipynb`](./lego_ai.ipynb) and run all cells.

## Model Evaluation

Model evaluation data can be found in [`model_eval.md`](./model_eval.md).
