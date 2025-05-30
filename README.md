Code for the Quadratic-Chi histogram distance
---------------------------------------------
Ofir Pele 
Contact: ofirpele@gmail.com
Version: 1.0, Aug 2010

This directory contains the source code for computing the Quadratic-Chi histogram distance
efficiently and examples of usage.

Please cite this paper if you use this code:\
 The Quadratic-Chi Histogram Distance Family\
 Ofir Pele, Michael Werman\
 ECCV 2010

```latex
@INPROCEEDINGS{Pele-eccv2010,
author = {Ofir Pele and Michael Werman},
title = {The Quadratic-Chi Histogram Distance Family},
booktitle = {ECCV},
year = {2010}
}
```

Easy startup
------------
Within Matlab:

```Matlab
demo_QC1 % 1d histograms
demo_QC2 % 3d histograms, SIFT
demo_QC3 % d-dimensional sparse histograms of different size
demo_QC4 % 5d (x,y,L*,a*,b*) histograms - color images comparison
help QC
```

In C++:
- demo_QC_full_sparse.cpp
- demo_QC_sparse_sparse.cpp (sparse_sparse can be useful for bag-of-words/bag-of-features, I did not make a Matlab version yet).

Compiling (the folder contains compiled binaries, thus you might not have to compile)
-------------------------------------------------------------------------------------
Within Matlab:

```Matlab
compile_QC
```

In a linux shell:
```Bash
make
```

Usage within C++
----------------
Full documentation is in the Matlab files. Note that Matlab demo scripts are good examples for QC usage.

Tips
----
- The speed increases with sparse bin-similarity matrices which inversely correspond to thresholded distances. 
- In my experience the performance usually increases with the threshold until a maximum and then it starts to decrease.
