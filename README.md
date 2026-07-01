# Project Overview
This code is for a project I was apart of from June 2023 to May 2025 during my last two years at Winona State University in Winona, Minnesota. I had the privilege of working
with two physics professors at my school. My project was a part of a larger, collaborative project with students and faculty from Cornell University in Ithaca, New York.
The project is called ZINGRS which stands for Zeus INvestigated Galaxy Reference Sample. Zeus is the name of a telescope which was used to detect galaxies around
redshift ('z') 1, which is 7 billion light years away from us here on Earth. Then, once the galaxies were selected, each were observed by the Very Large Array or VLA which
is located in Socorro County, New Mexico. Most of the galaxies were observed in two radio bands. There are roughly 30 galaxies in total that were included in ZINGRS.

## My Contributions

### Part I: CASA

The first part of the project I worked on, which is not this code that is shown here, involved using a software called Common Astronomy Software Applications or 
[CASA](https://casa.nrao.edu/). CASA uses a Interactive Python (IPython) environment for command line scripting. I used CASA for data reduction, data analysis, calibration of
atmospheric and phase calibrator errors, and imaging. Since the data sent back from the VLA ranged anywhere from 35 to 80 Gigabytes, and the tasks meantioned above are 
computationally expensive, I used a Virtual Machine to run CASA. The goal of this part is to reduce each band of each galaxy and to get each image in each band of all the 
galaxies in ZINGRS. I also found images of the same galaxy in different radio bands and using CASA, I checked to see if there was a detection. If there was, the image was used 
in the project.

### Part II: Image Gathering

This part didn't have any coding involved in it but it was a crucial step. In this step, I put all the images I found/made and other students made from part one into a folder 
that corresponds to the galaxy they belong to. I will explain the importance of this in the next step.

### Part III: Jupyter Notebook (The Code Shown Here)

Once everything in part one was complete, the next task was designing the code in this repository. I wrote most of the code but I had help from the physics professors I worked for.
The broad goal of the code is to visually display each galaxies radio contours by making a subplot for each galaxy. I will explain the key steps of the code in more detail. The first 
step the code takes is going to the folder path I gave it. Inside the folder are more folders named after each galaxy in the project. Inside those folders are the 
[.fits](https://heasarc.gsfc.nasa.gov/docs/heasarc/fits.html) images from part two which the code searches each folder for. Each galaxy has a background image selected which is either 
a CBand or KuBand. Once a background image is selected, the code reads each fits image in the folder. Each fits image contains valuable information about the image and this code extracts 
that information. This is how everything in each galaxies subplot is shown. If you click on the code and scroll down a bit, you are able to see the final output.
