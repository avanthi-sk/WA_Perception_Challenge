# WA_Perception_Challenge

answer.png
![answer1](https://github.com/user-attachments/assets/d9e4e0ed-e9c9-40d8-80de-544f671e15b1)


Methodolgy
I read in an image and converted it to an hsv image, since i wanted it to detect the cones based on color. I then created range of values that make red, and created a mask that is applied to the hsv image to isolate red areas, which could be potential cones. I then got all the contours of the image and iterated thorugh all of them.  Through the iterations, I checked the size of the contour to see if it would fall in what I approximated was the sizes of the cones.  If they did fall in the range, the centroid of the contour was calculated, and  was placed into either the left or right array, which corresponded to which half of the image they were positioned in. I then sorted the centroid positions based on y-axis, so that the line is drawn from the bottom up. I then used those points to find the best fit line (slope and intercept) to create a regression line.
What did you try and why do you think it did not work.
I first tried to make the contours on a gray scale image, and was going to try to get the contours of the cones based on location, but I realized too many contours were there to the point where it was unable to isolate just the cones.  
What libraries are used
I used OpenCV, Numpy, and Google Colab Patches
