# Computer-Vision-Rubiks-Cube
Object Recognition and Color Classification for Solving a Rubik’s Cube

## CVRubiksCube:
- The program should be run in the MATLAB application, not on the terminal.
- By default, all tests and a sample "proper" run are ran.
- As mentioned in the paper, this program has two steps:
    - Rubik's cube recognition
    - Color classification

## Images Datasets (on Images folder):
- Contains sets of six images that are input into the program.
- ImgTest-scale, ImgTest-translation, ImgTest-rotation, ImgTest-background, and ImgTest-lighting: are meant to test the Rubik's cube recognition algorithm. Running the tests corresponding to these image sets will output images with identified lines (and corners) of the Rubik's cube.
- ImgTest-color1, ImgTest-color2, and ImgTest-color3: are meant to test the color classification algorithm. Running the tests corresponding to these image sets will output text files containing information about the color of each sticker. These tests are performed by doing a regular full run of the algorithm. They are called tests because they were used to find qualitative results regarding the accuracy of the algorithm and because the six images in each set do not represent a cube space (they are merely composed of six random images of cube faces that are correctly recognized by the cube recognition algorithm). Please note that these tests are actually full runs of the entire program, but are not considered proper runs because the specific image sets are not proper (see below).
- ImgRun-1: an example of a proper set of images.
    - The cube is in a particular state.
    - There is one image per face of the cube.
    - The images are in the following order: yellow, orange, blue, red, green, white.
    - All of these conditions are necessary in order to be able to feed the output of this program to my C++ solver program. This is why I call this a "proper run" image set as opposed to a test image set.


## Expected Results:
- ExperimentsExpected: contains the expected .jpg or .txt file corresponding to each test image set
- stickers-set1Expected: contains the expected text output corresponding to the run image set


## Actual Results:
- Experiments: will contain the outputs of running each test. Once the tests are ran, they can be compared to the expected results in ExperimentsExpected
- stickers-set1: file that will be created when we run the algorithm on the IMgRun-1 image set. It can be compared to the expected results in stickers-set1Expected


## CroppedImage:
- Contains intermediate results of the algorithm (ROI's). Whatever is there at the moment is not relevant. It only matters for the program and is taken care of during runtime.

## Runtime:
- Doing a full run of all tests plus the sample proper run takes a while.
- Doing just the proper run should take about 25 seconds.
