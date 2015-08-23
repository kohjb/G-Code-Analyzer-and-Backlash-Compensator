# G-Code-Analyzer-and-Backlash-Compensator

I was having printouts that I felt were related to backlash except that I had trouble confirming it from examining the code. The key question I had was why the backlash error (a vertical "empty" column) was asymmetrical. So I created a program to examine the G-Code (which I had already wanted but didn't find any satisfactory ones), as well as to simulate some backlash.

The program is still certainly in beta mode, so do provide any feedback. I only had the program interpret the G-Code that I encountered in Cura, so other variants may not be interpreted correctly yet.

Some key features:

* Graphical Interface - hopefully easy to use, but do provide feedback
* Loaded G-Code is Interpreted to provide color codes. Easier to debug.
* 3D model - Rt-Click+Drag to rotate the object. Lt-Click+Drag to rotate your viewpoint. Mousewheel to Zoom. Uses OpenTK so it should be fast.
* Easy Visualization
  * Zoom in to see individual segments. 
  * Choose Solid, Layers, or Rainbow color coding of segments. 
  * See the whole 3D object, or by layer, or by line segment(s). 
  * If you select by layer or segments, the corresponding lines in the G-Code window are selected so you know which lines are responsible.
  * You can select one or more lines in the G-Code window, and it will just draw those lines in the 3D window! Great for debugging.
* See Backlash
  * Use the Backlash section to introduce some backlash
  * See the effects updated real time. I saw my "empty" column appear - which was an a-ha moment! My printer was indeed suffering from backlash. 
  * You can adjust the backlash to match your printout, and therefore deduce the backlash in your system - in X, Y. Not implemented Z yet.
* If you get "lost" moving around the 3D, click the Reset button. Known Bug: Sometimes the 3D window doesn't refresh - clicking with the Rt-Button will update the window.

Here's the Sequence you can use to download, install, and get familiar with the program:

1. Download the zip file here (https://github.com/kohjb/G-Code-Analyzer-and-Backlash-Compensator/blob/master/G-Code%20Analyzer.zip?raw=true). Extract the files to a location and run the file "G-Code 3D Print Analyzer.exe". If Norton or other Antivirus program pops up, you'll have to trust that I'm not writing malicious code I'm afraid so will need the more knowledgeable ones to help vouch for this.
* The program should run Maximised. But you can resize as needed.
Load G-Code from a file. If you need a sample, let me know. I've only tested with G-Code from Cura so far, and then again, only for very simple models.
* Try the 3D interaction to examine the 3D object. Press Reset if you get "lost". You can manually adjust the camera position, Zoom, and Target point as needed. Auto-Aim "locks" the view to the centre of the 3D object.
* Try drawing in different colors. I like Layers the best. It alternates between 2 colors. Checking "Slow" will slow down the Drawing for one frame only - it sort of simulates/animates the print.
* Try selecting Single Layer, and From-To. Layer shows only 1 layer. From-To shows by individual segments. The corresponding lines of G-Code are selected to help debugging (or learning G-Code).
* Try selecting one or more lines in the G-Code window. See the 3D update.
* If you need to see the original, raw G-Code, click the Show Source radio button.
* Set to Single-Layer, and view Layer 1 from Top view. Then try increasing the X or Y backlash values - by clicking their up-arrows. See the effects update on the screen.
* Work in Progress - Click the "Compensate Code" button to compensate for the backlash, and create Compensated G-Code! You can see the Compensated G-Code by clicking the Show Compensated button. You can then Save the Compensated G-Code to a file. Send it to your Printer to see if it prints out better. (as of this writing, haven't tried this yet!).

Feedback certainly welcome as to bugs, features/improvements, or just comments!
