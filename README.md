# **Gesture2Health**

Gesture2Health is an innovative project that aims to bridge the communication gap between hearing-impaired patients and healthcare professionals in India.  There are an estimated 18 million hearing-impaired individuals in India. Many healthcare professionals are not trained in ISL or other sign languages. The system uses a camera to capture the patient's gestures, which are then processed and analyzed by the model. The model then generates written text output, which can be used by healthcare professionals to communicate with the patient. 

Gesture2Health is not just a technological solution, but also a social one. The project is designed to promote greater awareness and understanding of the needs of hearing-impaired patients in healthcare settings and to promote more inclusive and equitable healthcare services. By developing a sign language recognition model trained on an Indian dataset for the healthcare domain, Gesture2Health is helping to bridge the gap between hearing-impaired patients and healthcare professionals, and creating a more just and equitable healthcare system for all.
    
## Table of Contents
* [Technologies and Tools](#technologies-and-tools)
* [Setup](#setup)
* [Demo Video](#demo-video)
* [contact](#contact)

## General Info

## Technologies And Tools
The following technologies and tools were used for the implemetation of our project:
- Python
- Mediapipe
- OpenCV
- TensorFlow
- Keras
- NumPy
- Fastdtw

## Setup
The project was implemented in Google Colab:
- Install the required dependencies mentioned below:
```python
!pip install mediapipe
!pip install opencv-contrib-python
!pip install tensorflow
!pip install fastdtw 
```
- Download the dataset:
    - The dataset is present in the folder named `Basic_Signs_Dataset`
    - This folder consists of `16` sub-folders (one sub-folder for one gesture) , where each sub-folder consists of video samples for one sign language to be trained.
 - Run each cell of `DTW.ipynb` file one by one.
    - First, we extract 18 frames of each video and then extract keypoints from each frame using mediapipe. Pose consists of 99 keypoints, left hand and right hand each consist of 63 keypoints. So the total keypoints extracted are 225.
    - After extracting the keypoints, we save it to `train_output.csv` file, where first 225 columns are of keypoints and 226th column consists of frame numbers of each video and 227th coulmn consists of the labels for the corresponding videos.
    - After that we perform the preprocessing and then divide the dataset i.e, csv file into train and test sets(70:30)
    - After that we apply the `DTWClassifier` and train it on our dataset.
    
## Demo Video
You can find the demo video of how our project works over [here]()

## Status


## Contact
