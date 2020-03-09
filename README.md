# Object_Detection
the directory contains these files.
├── images
│   ├── baggage_claim.jpg
│   ├── dining_table.jpg
│   ├── living_room.jpg
│   └── soccer.jpg
├── output
│   ├── airport_output.avi
│   ├── car_chase_01_output.avi
│   ├── car_chase_02_output.avi
│   └── overpass_output.avi
├── videos
│   ├── airport.mp4
│   ├── car_chase_01.mp4
│   ├── car_chase_02.mp4
│   └── overpass.mp4
├── yolo-coco
│   ├── coco.names
│   ├── yolov3.cfg
│   └── yolov3.weights
├── yolo.py
└── yolo_video.py

The directories (in order of importance) are:

yolo-coco/ : The YOLOv3 object detector pre-trained (on the COCO dataset) model files. These were trained by the Darknet team.
images/ : This folder contains four static images which we’ll perform object detection on for testing and evaluation purposes.
videos/ : After performing object detection with YOLO on images, we’ll process videos in real time. This directory contains four sample videos for you to test with.
output/ : Output videos that have been processed by YOLO and annotated with bounding boxes and class names can go in this folder.

We’re reviewing two Python scripts — yolo.py  and yolo_video.py . The first script is for images and then we’ll take what we learn and apply it to video in the second script.

Our command line arguments include:

--image : The path to the input image. We’ll detect objects in this image using YOLO.
--yolo : The base path to the YOLO directory. Our script will then load the required YOLO files in order to perform object detection on the image.
--confidence : Minimum probability to filter weak detections. I’ve given this a default value of 50% (0.5 ), but you should feel free to experiment with this value.
--threshold : This is our non-maxima suppression threshold with a default value of 0.3.
 
 command line:
 YOLO Object Detection with OpenCV
$ python yolo.py --image images/baggage_claim.jpg --yolo yolo-coco
[INFO] loading YOLO from disk...
[INFO] YOLO took 0.347815 seconds

thats it we have done object detection on images. 
 for any queries please go through this reference link:https://www.pyimagesearch.com/2018/11/12/yolo-object-detection-with-opencv/






