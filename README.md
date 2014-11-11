ImageGraphCut3DSegmentation
===========================

An extensions of ITKs (D Doria) 2D Graph cut segmentation to 3D grayscale images


Getting the code
----------------


Overview
--------
This software allows the user to perform a foreground/background segmentation of an image.
This implementation is based on "Graph Cuts and Efficient N-D Image Segmentation" by Yuri Boykov (IJCV 2006).

License
--------
GPLv3 (See LICENSE.txt). This is required because of the use of Kolmogorov's code.

Build notes
------------------
```
$ mkdir build
$ cd build
$ ccmake ../ 
  'c'
  set Release
  set /home/visualcomputing/code/InsightToolkit-4.4.2/build
  'c'
  Set build tests to OFF
  Set build examples to ON
  'c'
  'g'
$ make
```

Dependencies
------------
- ITK >= 4

If tests enabled: 
- Boost >=1.55

Example
-------
```
$ cd data/femur

$ ../../build/Examples/ImageGraphCut3DSegmentationExample input.mhd foreground.mhd background.mhd result.mhd 50 0 1

```
