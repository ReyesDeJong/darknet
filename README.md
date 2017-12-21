## Darknet for Pepper Robot

**Warning: avoid `sudo` use**

This is an implementation based on [Darknet](http://pjreddie.com/darknet), that is slightly modified to compile in Pepper robot.

Main modifications are:

  - comment `typedef struct network network;` on inclued/darknet.h
  - comment `clock_gettime(CLOCK_REALTIME, &now);` in `what_time_is_it_now()` function of src/util.c, and make respective modifications in several scripts to use the time measuring function `get_wall_time()`.


![Darknet Logo](http://pjreddie.com/media/files/darknet-black-small.png)

#Darknet#
Darknet is an open source neural network framework written in C and CUDA. It is fast, easy to install, and supports CPU and GPU computation.

For more information see the [Darknet project website](http://pjreddie.com/darknet).

For questions or issues please use the [Google Group](https://groups.google.com/forum/#!forum/darknet).

## Train example:

./darknet detector train cfg/person.data cfg/tiny-yolo-voc-layer.cfg tiny-yolo-voc.weights 

## Validation Recall Example 

./darknet detector recall cfg/person.data cfg/tiny-yolo-voc-layer.cfg tiny-yolo-voc.weights 
