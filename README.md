# dual_quaternion_registration
Instructions:
  1. Download and extract the folder.
  2. Generate CMAKE files into the build folder with the provided CMakeLists.txt (cmake-gui recommended. For installaztion and
     use instructions please see the end)
  3. Switch into the build folder in an open terminal and type "make".
  4. An executable file "registration" will be generated under path "build/devel/lib/dual_quaternion_registration/".
  5. Move into the directory where your executable file is generated.
  6. Run the executable file in the format of <br /><br />
              ./registration -m ../../../../data/(moving data file name) -f ../../../../data/(fixed data file name). <br /><br />
      a. -m is the flag followed by moving pointcloud file, -f is the flag followed by fixed pointcloud file. They are not     
      interchangeable <br />
      b. Please make sure to include the relative path ../../../../data/ and follow it by the name of the data file found in the
      data folder<br />
      c. If no data file provided, ptcld_moving2.txt and ptcld_fixed2.txt are used.<br />
      
  7. If no error occurs, you'll get the registration result in terminal.<br /><br />
      
  You can change the parameters passed into initialiation in registration_est_kf_rgbd.cpp and re-make to apply changes. 



# cmake-gui installation and usage
1. Download and install cmake version that matches your OS. https://cmake.org/
2. Once cmake installed and configured:<br />
   a. Go into the dual_quaternion_registration folder extracted out<br />
   b. Make a build directory<br />
   c. Open up cmake gui (type cmake-gui in terminal)<br />
   d. Set source directory to dual_quaternion_registration<br />
   e. Set build directory to one we just made<br />
   f. Once you press configure, a menu should pop up asking which generator to use. Select one according to your OS.<br />
   g. Ignore the toolset and compiler options. Native should work fine.<br />
   h. Click generate.<br />
   i. The cmake files should be generated into you build directory
