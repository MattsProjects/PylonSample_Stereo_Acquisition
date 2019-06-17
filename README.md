# PylonSample_Stereo_Acquisition
Acquires from two cameras (GigE or USB), and stitches the images side-by-side (does not do 3D construction).

PylonSample_Stereo_Acquisition.cpp:
- This sample supports Pylon 3.0 and higher
- Supports GigE or USB cameras (selected at compile time).
- When using GigE cameras, the cameras' free run acquisition is synchronized with the IEEE1588 (PTP) protocol.
- Images are stitched together side-by-side using the StitchImage.h library.
- Sample demostrates saving images as a .mp4 movie (using Pylon supplemental package found at www.baslerweb.com).
- Sample demostrates saving images as a .avi movie (using built-in Pylon libraries on Windows, and OpenCV on Linux).

PylonSample_Stereo_Acquisition_UniversalInstantCamera.cpp:
- This is a slightly different version of PylonSample_Stereo_Acquisition which uses the new "Universal Instant Camera" added in Pylon 5.2
- The "Universal Instant Camera" allows for selection of camera interface at runtime instead of at compile time.
- This is the same as using Pylon's GenAPI, but the Universal Instant Camera is more convinient than that.
- This sample can therefore support a mix of cameras at runtime (e.g. Left Camera can be GigE while the Right Camera is USB).

Note:
- These samples currently only demostrates acquisition of images. No image processing for 3D reconstruction is done.
