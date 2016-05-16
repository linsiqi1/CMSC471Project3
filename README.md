# CMSC471Project3
Image recognition program using opencv
**Please email linsiqi1@gmail.com or linsiqi1@umbc.edu if you have trouble set up the enviornment**

1. Make a directory called Proj3SiqiLin

2. Download CMake on https://cmake.org/download/
        - Select **cmake-3.5.2-Darwin-x86_64.tar.gz**
	- Extract **cmake-3.5.2-Darwin-x86_64.tar.gz**
3. Download opencv source code
	- Go to http://opencv.org/
	- Click OpenCV for Linux/Mac
	- Extract opencv-3.1.0.zip 
	- Move the extracted opencv-3.1.0 directory under the Proj3SiqiLin directory
	- Open the opencv-3.1.0 directory
	- Under the opencv-3.1.0 directory, Create a folder, name it "build"
4. Launch CMake
	- Under "where is the source code", enter the absolute path for where the opencv source code is located, which would be something like **……/Proj3SiqiLin/opencv-3.1.0**
	- Under "Where to build the binaries", enter the path for the "build" directory we just created, my path is **……/Proj3SiqiLin/opencv-3.1.0/build**
	- Click on the **Configure** button
	- After Configure is completed, click on the **Generate** button
	- Exit CMake after "Generate" is completed
5. Open Terminal
	- cd to the build directory under opencv-3.1.0
		**cd ……/Proj3SiqiLin/opencv-3.1.0/build**
	- enter the following command
		**make**
		**sudo make install**

6. Open the project in XCode
	- Click on the project
	- Click on the build settings
	- Type **Search paths**
	- Set **Always Search User Paths"** to "Yes"
	- Set **Framework Search Paths** to "/usr/local/lib"
	- Set **Header Search Paths** to "/usr/local/include"
	- Set **Library Search Paths** to the /build/lib directory under the opencv-3.1.0 directory, which woul be something like
		**……/Proj3SiqiLin/opencv-3.1.0/build/lib**
	- Right click on the Project, select "Add Files to Project3"
	- Go to the build/lib directory under ……/Proj3SiqiLin/opencv-3.1.0/build/lib, add the following four dylib items
		* libopencv_ml.3.1.0.dylib
		* libopencv_imgcodecs.3.1.0.dylib
		* libopencv_highgui.3.1.0.dylib
		* libopencv_core.3.1.0.dylib

7. Import the Test data into the project
	- Right Click the Project 3 executable under the Project directory on the project exploerer panel at the left hand side of Xcode
	- Select **Show in Finder** 
	- Copy the Data directory into the same directory that Project 3 Executable is located.
8. Set the command line arguments in XCode
	*  On the menu bar, select Product>Scheme>Edit Scheme>
	* Enter the file path of the image you wish to test under "Arguments Passed on Launch"



