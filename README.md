#DESCRIPTION

The pipeline to solve the images is described here:
    1.Import the necessary libraries and read the image.
    2.Convert the image to gray scale using .cvtColor
    3.The kernel size is set and Gaussian blur is applied for smoothening.
    4.Canny edge detection is used to detect the lane lines. the necessary parameters are specified.
    5.A four sided polygon is used to mask the edges.
    6.Hough transform is implememnted on the edge detected image.
    7.Lines are drawn and a color binary image is combined.

The pipeline to solve the video is described here:
    A video is a series of images. Here, the video is captured using cv2.VideoCapture and then read frame-by-frame in cv2.
    A delay of 40 is set to match the original frame per seconds.
    All the stepps applied for the image are carried out in a while loop.


#SHORTCOMINGS

    The code is slightly struggles to pick up road curves in the distant.
    Lines are also applied to tree shadows in the video, thereby depecting shadows as lanes.


#IMPROVEMENTS

    The values of the vertices of the four sided polygon need to be experimented with.
    The shadow problem needs to be solved.