## Prerequisites
  
- OpenCV Contrib Repository: https://github.com/opencv/opencv_contrib

          # 1. Install dependencies
          sudo apt update && sudo apt install -y cmake g++ libgtk-3-dev libtbb-dev
          
          # 2. Clone OpenCV and contrib
          cd ~
          git clone https://github.com/opencv/opencv.git
          git clone https://github.com/opencv/opencv_contrib.git
          
          # 3. Build and install
          cd opencv && mkdir build && cd build
          cmake -D CMAKE_BUILD_TYPE=Release \
          -D CMAKE_INSTALL_PREFIX=/usr/local \
          -D OPENCV_EXTRA_MODULES_PATH=~/opencv_contrib/modules ..
          make -j$(nproc)
          sudo make install
          pkg-config --modversion opencv4

- RealSense SDK : https://github.com/IntelRealSense/librealsense/blob/master/doc/installation.md

### Build and Run

          # 1. Clone the repository
          git clone https://github.com/ichsanyudika/RealSense_Segment.git
          
          # 2. Build
          cd RealSense_Segment
          mkdir build && cd build
          cmake ..
          make
          
          # 3. Run the application
          ./cam

### Results

![](output/output.png)
