## Object Counting YOLOv7

## How to run with Google Colab

1. Clone project

```json
!git clone https://github.com/thanhnguye135/object_counting_yolov7.git
%cd object_counting_yolov7

!pip install -r requirements.txt
```

2. Get dataset from coco

```json
!bash scripts/get_coco.sh
```

3. Training model

```json
!python train.py --weights yolov7.pt --cfg cfg/training/yolov7.yaml --data data/coco.yaml --epochs 50 --batch-size 8 --img 416 --device 0 --cache-images
```

4. Detect and counting object

```json
!python detect.py --weights yolov7.pt --conf 0.25 --img-size 640 --source inference/images/image2.jpg
```
