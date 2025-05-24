# LEGO® Bricks Detection

This repository contains LEGO® bricks detection & shape/color classification models trained on YOLO and ResNet. Both combined they detect pieces on an image and match them to their respective piece ID and color ID.

Dataset: [https://www.kaggle.com/datasets/ronanpickell/b100-lego-detection-dataset](https://www.kaggle.com/datasets/ronanpickell/b100-lego-detection-dataset) \
LEGO® Catalog: [https://www.lego.com/en-us/pick-and-build/pick-a-brick](https://www.lego.com/en-us/pick-and-build/pick-a-brick)

All created models can be found in `models` directory.

## The idea

The whole premise of this project is to create a system that will detect LEGO® bricks and classify them by shape and color. The system consists of two models. The first one (based on Yolo8m) is used to detect one of 200 brick classes from the photo. The second one (based on ResNet50) is then used to detect on of 40 color variants.

## Assumptions

There are 40 colors, many of which are quite similar. This similarity reduces the model's accuracy. To address this, we grouped the `m[number]` colors into broader, more abstract superclasses:

```py
color_groups = {
    'yellow': ['m0', 'm13'],
    'orange': ['m1', 'm21'],
    'red': ['m2', 'm35'],
    'pink': ['m3', 'm14', 'm22'],
    'purple': ['m15', 'm23', 'm28'],
    'blue': ['m4', 'm16', 'm24', 'm36', 'm5', 'm17'],
    'gray': ['m29', 'm27', 'm34', 'm18'],
    'green': ['m6', 'm30', 'm25', 'm7', 'm37', 'm8', 'm31'],
    'brown': ['m9', 'm19', 'm26', 'm32', 'm38', 'm10', 'm20', 'm33'],
    'white': ['m11', 'm12'],
    'black': ['m39']
}
```

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

4. Open [`lego_yolo.ipynb`](./lego_yolo.ipynb) and run all cells.

5. Open [`lego_cnn.ipynb`](./lego_cnn.ipynb) and run all cells (WARNING: can take a long time).

## Model Evaluation

Model evaluation data can be found in [`model_eval.md`](./model_eval.md).
