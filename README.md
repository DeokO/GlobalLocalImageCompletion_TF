# Globally and Locally Consistent Image Completion

Tensorflow implementation of Globally and Locally Consistent Image Completion on [celebA](http://mmlab.ie.cuhk.edu.hk/projects/CelebA.html) dataset.  
![Alt text](images/network.JPG?raw=true "network")
데이터 다운로드: https://www.kaggle.com/jessicali9530/celeba-dataset

## What's different from the paper  
* smaller image input size (64x64)  
* smaller patch sizes  
* less number of training iteration (500,000 iterations in the paper)
* Adam optimizer used instead of Adadelta

## Requirements
* Opencv 2.4
* Tensorflow 1.4

## Folder Setting
```
-data
  -img_align_celeba
    -img1.jpg
    -img2.jpg
    -...
```


## Train
```
$ python train.py 
```

To continue training  
```
$ python train.py --continue_training=True
```

## Test  
Download pretrained weights  
```
$ python download.py
```

```
$ python test.py --img_path=./data/test/test_img.jpg
```

![Alt text](images/res.gif?raw=true "result gif")  

Use your mouse to erase pixels in the image.  
When you're done, press ENTER.  
Result will be shown in few seconds.  


## Results  
![Alt text](images/res.png?raw=true "result")
