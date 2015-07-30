Simple Vehicle Detection, Tracking, and Counter
========================================

##Overview
1. First, we need to detect moving vehicles. An easy way to do this is is by using a Background Subtraction algorithm.
2. To track these vehicles, we can use a blob tracking algorithm (such as [cvBlob](https://code.google.com/p/cvblob/) or [OpenCVBlobsLib](http://opencvblobslib.github.io/opencvblobslib/)). Using the **cvBlob** library, we can track the **centroid** of each vehicle.
3. Then, to count the vehicles, check if the **centroid** of the moving objects have crossed a static line in the video.

##Features
* Basic setup includes setting two different lines. The red line divides states `A` and `B`, while the green line divides states `C` and `D`.

##Additional information:
* There is a Visual Studio 2013 template project in the `vs2013/` folder. Open it in the Visual Studio IDE and select [Release]-[Win32] mode.
* The include files for the OpenCV 2.4.10 are provided in the `include/` folder, and the related static libraries are provided in the `lib/x86/vc12/` folder.
* The `dataset/video.avi` file will need to be re-encoded to RAW format for OpenCV. You can use [ffmpeg](https://www.ffmpeg.org) and run `ffmpeg -i video.avi -vcodec rawvideo video_raw.avi` to do this.
