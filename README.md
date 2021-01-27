# Real-time-Face-mask-detector
In this time of the pandemic, wearing masks is mandatory. So I came up with an idea. An idea about making a real-time mask detection model using Python and ML. Eventually, this became my topic for the Artificial Intelligence project in college.

So without any further delay, let's dive right into it! [CODE AVAILABLE IN MASTER BRANCH]

# Hardware Requirements:

1. Quad-core processor(Intel/AMD) or higher

2. Dedicated NVIDIA GPU(Mx 250M or higher/GTX 750 Ti or higher)

3. 8GB 2333MHz RAM or higher

# Software Requirements:

Be very careful while installing all the required software, as incompatible software versions will cause conflicts in the upcoming steps. Install these ones one by one:

1. Anaconda - https://www.anaconda.com/products/individual

2. Python 3.8 - https://www.python.org/downloads/release/python-380/

3. Visual Studio - https://visualstudio.microsoft.com/downloads/

4. CUDA Toolkit - https://developer.nvidia.com/Cuda-Toolkit-Archive

5. CuDNN - https://developer.nvidia.com/rdp/cudnn-download

# Follow these steps to install CuDNN:

1. Download the latest cuDNN for CUDA 11.1

2. Download the library for Windows 10

3. Extract the contents of the zip file (i.e. the folder named cuda) inside <INSTALL_PATH>\NVIDIA GPU Computing Toolkit\CUDA\v11.1\, where <INSTALL_PATH> points to the installation directory specified during the installation of the CUDA Toolkit. By default <INSTALL_PATH> = C:\Program Files

![](fe1.png)

# Setting up the environment -

1. Go to Start and Search “environment variables”

2. Click “Edit the system environment variables”. This should open the “System Properties” window

3. In the opened window, click the “Environment Variables…” button to open the “Environment Variables” window.

4. Under “System variables”, search for and click on the Path system variable, then click “Edit…”
Add the following paths, then click “OK” to save the changes:

       <INSTALL_PATH>\NVIDIA GPU Computing Toolkit\CUDA\v11.1\bin

       <INSTALL_PATH>\NVIDIA GPU Computing Toolkit\CUDA\v11.1\libnvvp

       <INSTALL_PATH>\NVIDIA GPU Computing Toolkit\CUDA\v11.1\extras\CUPTI\libx64

       <INSTALL_PATH>\NVIDIA GPU Computing Toolkit\CUDA\v11.1\cuda\bin
    
![](se.png)

# Download all the contents from this link:
  GitHub has reduced the dataset from 8600 images to just 2000. In order to increase the accuracy of your model, you can download all the images from the link given below
    
  http://bit.ly/Face-Mask-Detection

![](fe2.png)

# Steps for training the model begins:

1. Open "Anaconda Prompt" from the Start menu

2. Navigate to this above folder:

![](E.png)

3. Now run the following command:

       pip install -r requirements.txt
       
It will show the following screen -

![](requirements.jpeg)

After all the installations are over, it is finally time to train the model on our dataset.

### NOTE: 
This dataset folder contains two folders - "with_mask" and "without_mask". This basically contains two different types of images. One contains images of people wearing masks while the other one contains images where people are not wearing a mask.

Normally for such projects, 1500-2000 images are enough to train the model. But here I have used 8600 images just for the sake of 99.99% accuracy. This will take a bit longer time to analyze for each epoch(iterations) but it will be worth the wait.

4. Run the following code:

       python train_mask_detector.py

![](epoch.png)
It can take 30-50 minutes to run all the 20 epochs depending on your hardware configuration. Please wait patiently. It is advised not to do any CPU/GPU intensive tasks while this is being done.

# Difference in Accuracy

![](accuracy compare.jpeg)
### Now we are ready to test our model in real-time
Inside the same folder, open another Anaconda terminal(do not close the previous one). Now type the following line:

    python detect_mask_video.py

After a few seconds, a separate window will appear where you can see your live webcam video feed.

  ![](accuracy compare.jpeg))

Finally, we have finished making our model and we are getting pretty good results. You can try the same procedure for other projects on categorisation(like cats and dogs classifications) and more.

## Contact me through:
   WhatsApp: +91-7596985078
   
   Email: reetamdutta1@gmail.com
   
   Website: https://bit.ly/rdgraphics_website
