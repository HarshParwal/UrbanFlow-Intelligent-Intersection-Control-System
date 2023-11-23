# UrbanFlow-Intelligent-Intersection-Control-System
The deep learning model presented in this study leverages the YOLO (You Only Look Once) framework for object detection in the context of intelligent intersection control. The implementation on a Linux platform provides a reliable environment for deployment, offering flexibility and scalability.

The model's performance is evaluated using test images, showcasing its effectiveness in dynamically assessing traffic conditions. Notably, the model adapts signal timings based on the calculated density of vehicles, ensuring a responsive and adaptive traffic management system. The YOLO-based deep learning model stands as a powerful tool in enhancing intersection control, contributing to improved traffic flow, safety, and overall efficiency in urban environments.

Instruction to run the project :
1. **Install Git:**
   - Open a terminal and run the following command to install Git: 
     sudo apt-get install git
    

2. **Clone Darknet Repository:**
   - Change to the desired directory and clone the Darknet repository:
     git clone https://github.com/AlexeyAB/darknet

3. **Configure Makefile:**
   - Navigate to the Darknet directory:
     cd darknet

   - Open the `Makefile` in a text editor and modify the following settings:
     Makefile
     GPU=0
     CUDNN=0
     CUDNN_HALF=0
     OPENCV=1
     AVX=0
     OPENMP=0
     LIBSO=1
     ZED_CAMERA=0
     ZED_CAMERA_v2_8=0
     
   - Save the changes and exit the text editor.
   - Run the following command to compile Darknet:
     make
    
4. **Clone UrabanFlow Repository:**
   - Change to the directory where you want to clone the Intelligent Traffic Flow repository:
    
     cd ~  # Or choose your preferred directory
     git clone https://github.com/HarshParwal/UrbanFlow-Intelligent-Intersection-Control-System
    

5. **Copy Configuration and Data Files:**
   - Copy configuration and data files from the Intelligent Traffic Flow repository to the Darknet installation:
     cp -r UrbanFlow-Intelligent-Intersection-Control-System/cfg/* darknet/cfg/
     cp -r UrbanFlow-Intelligent-Intersection-Control-System/data/* darknet/data/
     
   - Copy the 'test_images' folder:
     cp -r UrbanFlow-Intelligent-Intersection-Control-System/test_images darknet/
     

6. **Copy Additional Files:**
   - Copy remaining files from the UrbanFlow repository to the Darknet installation:
     cp UrbanFlow-Intelligent-Intersection-Control-System/*.txt UrbanFlow-Intelligent-Intersection-Control-System/*.py UrbanFlow-Intelligent-Intersection-Control-System/*.weights darknet/
     

7. **Run the Program:**
   - Navigate to the Darknet directory:
     cd darknet
     
   - Run the Python script:
     python3 signalswitchalgo.py
     

Ensure that Python 3 is installed on your system, and consider installing any additional dependencies mentioned in the respective repositories.




