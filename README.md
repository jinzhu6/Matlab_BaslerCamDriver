# Matlab_BaslerCamDriver
A universal MATLAB driver for Basler cameras

Copyright (c) 2015 Hannes Badertscher

Until now, interfacing cameras in MATLAB is a cumbersome task. 
MATLAB offers no support for USB3 Vision cameras, and the GigE driver is rather buggy.
This driver package provides an open-source C++ interface between MATLAB and Basler's Pylon interface.

## Build

The MATLAB Basler Camera Driver is built by calling the provided `make.m` file.

###Requirements:
* [Boost C++ Libraries](http://www.boost.org/) (+ `BOOST_ROOT` set to the Boost root directory)
* [Basler Pylon 4](http://www.baslerweb.com/de/produkte/software) 

## Functions
* `baslerFindCameras` returns a cell array containing the camera index and the camera name.
* `baslerCameraInfo` returns a struct containing all parameters of the selected camera.
* `baslerSetParameter` sets a camera parameter.
* `baslerGetParameter` returns the selected camera parameter.
* `baslerPreview` displays a preview image.
* `baslerGetData` captures and returns the selected number of frames.
* `baslerSaveData` captures the selected number of frames and saves these to disc.
* `baslerSaveDataThread` capures and saves the selected number of frames without blocking MATLAB.

## License

The MIT License (MIT)

Copyright (c) 2015 Hannes Badertscher

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.