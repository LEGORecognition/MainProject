# Model evaluation

### Variation 1

```
Yolo11m
epochs=500
imgsz=512
batch=4
patience=10
```

Learning stopped at ~45 epochs \
mAP@50-95: 0.554 \
mAP@50: 0.630 \
mAP@75: 0.617

### Variation 2

[`lego_detection_yolov8m.pt`](./models/lego_detection_yolov8m.pt)

```
Yolov8m
epochs=500
imgsz=768
batch=4
patience=20
```

Learning stopped at 100 epochs \
mAP@50-95: 0.725 \
mAP@50: 0.795 \
mAP@75: 0.781
