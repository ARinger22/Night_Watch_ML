# Night_Watch

### An AI/ML model to find suspicious activity of cycle stealing using camera footage or videos.

## Tools Used
  <ul>
    <li>Google Colab & VS Code with libraries</li>
    <li>Yolov5 Architecture</li>
    <li>OpenCV</li>
  </ul>
  
## GitHub Repository Structure
  <ul>
    <li>dataset : Directory containing the dataset (images)</li>
    <li>Night_watch.ipynb : file takes the yolov5 real-time objective detection model then we give our dataset here to learn our dataset and it builds a model. Also adds bounding box if tested on an uploaded video.</li>
    <li>custom.yaml : Directory which gives the path of our dataset</li>
    <li>cycle_theft: file to run the model after downloading it with live webcam</li>
    <li>demo.mp4: file for testing the model</li>
    <li>problemStatement_year_4.pdf : problem statement of the problem</li>
  </ul>

## Working 
  ### 1. Data Collection and Training : 
  <ul>
    <li>Dataset : It consists of images for training and testing, including normal and suspicious events related to cycle theft. </li>
    <li>Training : Image frames were extracted and resized for compatibility with the model.</li>
  </ul>

  ### 2. Anomaly Detection : 
  <ul>
    <li>Confidence : The first step of thief detection is on its confidence level. The confidence level of the person detection should be at least 80 percent.</li>
    <li>Time Spent : The second step of thief detection is the time spent by the person to work on opening the lock. </li>
  </ul>
      <h5> If both conditions are satisfied, then our model prints "Hello, thief" on the console, declaring the presence of a cycle thief. </h5>


    
## How to run
  <ul>
    <li>Before running any terminal, ensure you are running your notebook on GPU instead of CPU. To check, go on runtime/change runtime type it should be on GPU (Can change it on Google Colab; in case you are running it on PC, make sure that your GPU is active while running this file).</li>
    <li>First download the ipynb file.</li>
    <li>Run the first kernel to download the some files and dependencies for yolov5.</li>
    <li>Now we need to add custom.yaml file inside the yolov5/data folder for the code to work furthur.</li>
    <li>Add the dataset folder into your drive. </li>
    <li>Run the second kernel of the notebook. It will connect to your drive to fetch the dataset.</li>
    <li>Now run the third kernel for prediction or model validation.</li>
    <li>Now to test the model that it is running fine, upload the demo.mp4 file inside your notebook.</li>
    <li>Now run the fourth terminal to run the model in our video.</li>
    <li>Download the video from the directory yolov5/runs/detect/exp2 then download the demo.mp4 file again and run it you will see some prediction there.</li>
  </ul>

## Run on live webcam
  to run on a live webcam 
  <ul>
    <li>First Download the last.pt model which after running the above steps. </li>
    <li>Download from the directory yolov5/models/last.pt model. </li>
    <li>Put the path of your last.pt model inside the cycle_theft.ipynb jupyter file in the path.</li>
    <li>After running make sure you have permission for your webcam to open then you will able to see that the model is working.</li>
  </ul>
  
### For more you see our presentation uploaded to the repository.

## Conclusion
  The cycle theft detection model combines the power of yolov5 architecture to identify suspicious events in video footage. By leveraging deep learning techniques, this model offers a reliable solution for enhancing security and preventing cycle theft incidents even in low light and poor image quality conditions.

<img src="Image1.png"/>
The above image is the screenshot of test image which captures the detected person, and shows confidence rate on the frame as well.

