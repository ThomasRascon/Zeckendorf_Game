This collection of programs displays the graph generated by an n-token accelerated Zeckendorf game. 
The data for these graphs is generated with c++ programs, while the GUI is a python program. 
For information on usage of the GUI, such as controls and parameters, see the documentation at the top of GraphColoring.py, or the bottom of this readme.

<h2>Setup:</h2>

<h4>Windows:</h4>
First download git and docker desktop. Docker desktop can be downloaded at the following link: <br>
https://docs.docker.com/desktop/install/windows-install/

Run the following command to copy the files from this repository to your computer: <br>
git clone https://github.com/ThomasRascon/ZeckGame-DecisionRecursion.git

Now open docker desktop to start docker, navigate to where this repository was cloned to on your computer, and run compileProgram.bat, followed by runProgram.bat <br>
If you close the program, and want to run it again without changing any parameters, simply run the file runProgram.bat again. If you change any parameters, you must run compileProgram.bat for your changes to be reflected in a run. If you turn off your computer, and want to run the program again, run docker desktop, and run runProgram.bat.

<h4>Mac/Linux</h4>
First make sure that you have git, python, and the g++ compiler installed, then run the fpllowing command to copy the files from this repository to your computer: <br>
git clone https://github.com/ThomasRascon/ZeckGame-DecisionRecursion.git

Then navigate to the folder where this repository is downloaded, and compile the c++ programs for use with the GUI. This is only ever necessary to do once: <br>
g++ -shared -o clibrary.so -fPIC -std=c++17 GraphStructure.cpp ZeckGame.cpp 

Then you may run the GUI with the following command: <br>
python3 GraphColoring.py

<h2>GUI Usage Instructions</h2>
The following parameters can be editted at the top of GraphColoring.py:

clib.build(n,0): The first argument n is the number of initial tokens          <br>
r:               Circle radius for base of arrows                              <br>
buttonWidth:     Width of buttons in pixels                                    <br>
buttonHeight:    Height of buttons in pixels                                   <br> 
grid_x:          Distance at which buttons are spaced in x direction in pixels <br>
grid_y:          Distance at which buttons are spaced in y direction in pixels <br>
windowWidth:     Width of GUI window in pixels                                 <br>
windowHeight:    Height of GUI window in pixels                                <br>
fontSize:        Size of font in buttons                                       <br>


<h4>Keyboard controls:</h4>
e - colors green<br>
q - colors purple<br>
w - toggles guess<br>
s - toggles variable "show" which determines if clicking a button erases all arrows on screen, which is on by default, meaning that arrows will not get erased when clicking<br>
a - shows all arrows for all connections<br>
z - undoes previous coloring<br>

