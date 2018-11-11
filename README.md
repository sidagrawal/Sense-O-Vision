# Sense O’Vision

Using `Sense O’Vision` (Blind Helper) will play a video loaded by a user at 1 fps (frames per second).
For every frame `Sense O’Vision` will generate sound by analyzing all pixels. Between each frame there
is a "click" sound to indicate the frame is changing. This program is meant for blind people who can use the
generated sound to understand what is displayed for every frame.

## Optional Implemented Features

Extra Functionality:
-Volume slider added which will adjust the volume of the sound outputted per frame, as well as the volume of the clicks. To implement this feature, the sound writes/outputs from SourceDataLine on a separate thread to allow for the sound and video to play concurrently. As the sound is output, if the user changes the volume slider, we measure the percentage of the slider, and adjust the volume accordingly. 
-Implemented stop processes to allow users to open another video without having to close down the program. Otherwise each thread would continue to run in the background even when the program is shut down.
-File chooser implemented to allow the user to choose their file through a popup box

GUI:
-The GUI was enhanced to follow norms that the graphic design industry follows. The interface and buttons are a dark grey at #535353 which allows for a less jarring visual feel for users who are not blind.
-Play/Stop button switches functionality between ‘Play’ and ‘Stop’. It will be ‘Play’ when the video is not playing, and ‘Stop’ when is playing
-Play/Stop button is disabled/greyed out when no video is loaded
