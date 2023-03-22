# Week 1

### Goal:

- Learn about the databases to be used: AICityChallenge and KITTI
- Implement evaluation metrics: Intersection over Union (IoU), Average Precision (AP), Mean Square Error in Non-Occluded
  areas, Percentage of Erroneous pixels in Non-occluded areas
- Analyze: Effect of noise additions, IoU vs Time, Optical Flow

&nbsp;

### Task 1 and 2

See Task1_Task2.ipynb

&nbsp;

### Task 3 and 4

See Task3_Task4.ipynb

&nbsp;

### Video Generation

Arguments:\
-m --run_mode : Gaussian, AdaptiveGaussian, SOTA\
-r --run_name : Run Folder Name\
-c --config   : config.yml path\
-s --save     : Save the video or not    [True, False]\
-d --display  : Show the video or not    [True, False]\
-p --percentage: Percentage of video frames to use as background\
-e --sota_method : [MOG, MOG2, LSBP, KNN,GMG ]\
-a --alpha: alpha values \
--rho: rho values \
-c --colorspaces: [gray, RGB, YCRCB, HSV, YUV]\
-g --grid: show the grid or not

#### Gaussian modeling

```
python main.py -r task_1 -m Gaussian -p 0.25 -c gray -a 5 
```

#### Adaptive Gaussian modeling

```
python main.py -r task_2 -m AdaptiveGaussian -p 0.25 -c gray -a 5 --rho 0.05
```

#### SOTA modeling

```
python main.py -r task_3 -m SOTA -p 0.25 -c gray -e MOG2 -a 0

```

#### Color modeling

```
 python main.py -r task_4 -m Gaussian -p 0.25 -c RGB -a 5
```


