# GCMP--Gesture_Control_Media_Player
Software that will recognize human hand gestures and operate the VLC media player based on the hand movements that is, it can increase or decrease the volume, pause or start the video, forward the track etc, without actually touching the keyboard. For this project, we have chosen VLC media player, but it can be extended to any application. 

## Objectives:

1.	To implement Face Recognition Lock System so that program runs only when a particular person unlock the system by his/her face.

2. 	To implement hand gesture recognition system using python and OpenCV.

3. 	To connect the Gesture Recognition system to control the VLC Media Player.

## Prerequisites:
1. You must have **opencv-contrib-python** installed in your system. In case you don't have then **clone or download** this project and    type these commands in command prompt/terminal.

      $ cd handy-master
      $ pip install -r requirements.txt

2. You must have python3 installed in your system.

3. You should be ready with dataset of sample images to be used for face recognition system. If images are in grayscale then the program    will execute faster.Give your path of dataset in the code.

#### To execute facial recogniton code:

   $python3 face_unlock.py

#### To execute hand gesture recogniton code:

   $ python test.py
   
   **NOTE: When the program starts, it'll pop open a web cam feed and you have to place a part of your hand in the rectangle shown and press the key 'a' to calibrate the system with your skin color and the detection process will start.**
   
## Module 1: Implementation of Face Recognition Locking/Unlocking system

The project begins with the face recognition of the authorized user. A model is trained by images of a person, i.e., the authorized person. As soon as that person’s face comes into the region of interest, a message pops up on to the screen with the name of the person and the program control goes on to the next module. So basically, this step focuses on the authentication using face recognition.

![](/face_unlock.png)

## Module 2: Implementation of Hand Gesture Recognition System

![](/hand_gesture_recog_process.png)


First our hands will be detected. After that, the program will separate the palm from the fingers and segment it into a different region. Then after, program will identify the fingers and capture it into the region. After that the gestures will be recognized. For example, if one finger up then it will show one, similarly for two fingers, open palm, closed fist etc. Each gesture will correspond to a separate control command which will be connected to the application in the last module.

![](/hand_gesture_recog.png)

## Module 3: Integrating VLC Media Player with Gesture Recognition System


In this module our program will be connected to the control devices such as mouse or keyboard. This will be done using one of the python modules- PyAutoGUI.  PyAutoGUI is a cross-platform GUI automation Python module for human beings. It is used to programmatically control the keyboard and mouse.

I am currently working on this module. So stay tuned.

For more information or suggestions, you can contact me through mail: **mridul.mark@gmail.com** 

## Result Analysis and Limitations:

**Objectives achieved so far is:**

- Implementation of face unlocking system and implementation of hand gesture recognition system. 

- Face Detection model is showing around 75%-80% accuracy. 

- Hand Gesture recognition model is showing 68%-72% accuracy. 

**The condition applied is that:** 

- Background color should not match with the palm color. 

- Background should be white (preferably). 

- Intensity of light should also be appropriate.
