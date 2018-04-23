[//]: # (Image References)

[image1]: ./rm_img/Grid.png
[image2]: ./output_images/undistortion.png "Undistorted"
[image3]: ./output_images/x_thred.png "x_thredx_thred"
[image4]: ./output_images/mag_thresh.png 
[image5]: ./output_images/dir_thresh.png
[image6]: ./output_images/s_thresh.png
[image7]: ./output_images/combined_all.png
[image8]: ./output_images/trans_on_test.png
[image9]: ./output_images/perspective_tran.png
[image10]: ./output_images/histogram.png
[image11]: ./output_images/sliding_window_search.png
[image12]: ./output_images/pipelined.png

[video1]: ./vedio_out/project_video_out.mp4 "Video"
## **车辆检测（YOLOV2)**

ps:本来是打算keras构建模型结构，然后加载weights文件训练后了参数实现的，但一直没有搞清楚weights文件的参数是怎么和模型各层对应上，所以最后找了可以

基于YOLOV2实现车辆检测

### YOLO简介：
YOLO意为 You Only Look Once，是一种基于深度学习的端对端（end to end）物体检测方法.与R-CNN,Fast-R-CNN,Faster-R-CNN等通过region proposal产生大量的可能包含待检测物体的 potential bounding box，再用分类器去判断每个 bounding box里是否包含有物体，以及物体所属类别的方法不同，YOLO将物体检测任务当做一个regression问题来处理.

### YOLO检测思路：
(这里以输入为416x416的YOLOV2为例)

首先将图片划分为13x13个栅格(grid cells):
![alt text][image1]




