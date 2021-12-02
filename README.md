# Blood Cancer Detection with YOLOV5

# Intrudiction

This notes that I took for target detection with yolov5. In this project, blood cancer cells were detected.


## Create an environment

* Update pip with the following command.
```bash
$ python -m pip install --upgrade pip
```
* Create an enviroment.
```bash 
$ conda create --name yolov5 
```
* Activate this environment
```bash
$ conda activate yolov5
```
## Requirements

* Open the yolov5 directory
```bash
$ cd <yolov5_dir>
```
* Setup requirements
```bash
 $ pip install -r requirements.txt
```
* Make sure you have cuda and cudnn installs

## Train

* Make sure environment activated. Go to yolov5 directory.
```bash
$ cd <yolov5_dir>
```

* Run commands below
```bash
% python train.py --img 416 --data ../data.yaml --cfg ./models/yolov5s.yaml  --batch 32 --epochs 50
```
* You can see the training results and  weights, enter the directory below in the yolov5 folder.

```bash
$ cd <yolov5_dir>/runs/train
```
## Detect

* Run commands below

```bash
$ python detect.py --source ../dataset/test/images/ --weights ./runs/train/exp/weights/best.pt --conf 0.4
```                                 
*  You can see the detection results, enter the directory below in the yolov5 folder.     

```bash
$ cd <yolov5_dir>/runs/detect
```
