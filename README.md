# Recognize, Crop and Save Faces as Images From Video

For technical details check the related [medium post](https://medium.com/@ahmetozlu93/creating-multi-view-face-recognition-detection-database-for-deep-learning-in-programmatic-way-14bbdd4b00a9)! ***Please contact if you need professional face detection & recognition project with the super high accuracy.***

## QUICK DEMO

- Faces are Tracking, Cropping and Saving as Images from Video

<p align="center">
  <img src="https://user-images.githubusercontent.com/22610163/30784383-d75e112c-a15c-11e7-88e9-ec9ded45f57b.gif">
</p>

- Images are Saving from Video With Appropriate Path Hierarchy

<p align="center">
  <img src="https://user-images.githubusercontent.com/22610163/30775206-0d959a3c-a098-11e7-965e-add626987376.gif">
</p>

## THEORY

<p align="center">
  <img src="https://user-images.githubusercontent.com/22610163/103477099-43bc1980-4dcc-11eb-95ae-510fd33e90c6.png" | width=300>
</p>

If you want to investigate some aspect of facial recognition or facial detection. One thing you are going to want is a variety of faces that you can use for your system. You can create your own face detection/recognition database by this program. [face_recognizer.py](https://github.com/ahmetozlu/face_database_creator/blob/master/face_recognizer.py) recognizes the faces from video, crop and save them as an image under appropriate path hierarchy.

Once we have acquired the face data, we’ll need to read it in our program. In the demo applications I have decided to read the images from a very simple CSV file. Why? Because it’s the simplest platform-independent approach I can think of. However, if you know a simpler solution please ping me about it. Basically all the CSV file needs to contain are lines composed of a filename followed by a ; followed by the label (as integer number), making up a line like this:

    /path/to/image.ext;0

You don’t really want to create the CSV file by hand. I have prepared you a little Python script [create_csv.py](https://github.com/ahmetozlu/face_database_creator/blob/master/create_csv.py) that automatically creates you a CSV file.
    
face_recognizer.py calls create_csv.py and it can save the output as a csv file so you will have your own face detection/recognition dataset.

## INSTALLATION

**1.) Python and pip**

Python is automatically installed on Ubuntu. Take a moment to confirm (by issuing a python -V command) that one of the following Python versions is already installed on your system:


- Python 2.7
- Python 3.3+

The pip or pip3 package manager is usually installed on Ubuntu. Take a moment to confirm (by issuing a *pip -V* or *pip3 -V* command) that pip or pip3 is installed. We strongly recommend version 8.1 or higher of pip or pip3. If Version 8.1 or later is not installed, issue the following command, which will either install or upgrade to the latest pip version:

    $ sudo apt-get install python-pip python-dev   # for Python 2.7
    $ sudo apt-get install python3-pip python3-dev # for Python 3.n
    
**2.) dlib**

Install dlib prerequisites

The dlib library only has four primary prerequisites:
Boost
Boost.Python
CMake
X11/XQuartx

Installing CMake, Boost, Boost.Python, and X11 can be accomplished easily with  **apt-get** :

    $ sudo apt-get install build-essential cmake
    $ sudo apt-get install libgtk-3-dev
    $ sudo apt-get install libboost-all-dev
    
    $ wget https://bootstrap.pypa.io/get-pip.py
    $ sudo python get-pip.py
    
Install dlib with Python bindings

The dlib library doesn’t have any real Python prerequisites, but if you plan on using dlib for any type of computer vision or image processing, I would recommend installing:


- NumPy
- SciPy
- scikit-image

These packages can be installed via pip :

    $ pip install numpy
    $ pip install scipy
    $ pip install scikit-image
    
Years ago, we had to compile dlib manually from source (similar to how we install OpenCV). However, we can now use pip  to install dlib as well:

    $ pip install dlib
    


