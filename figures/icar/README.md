LaTeX animation
===============

Build instructions
------------------
The files in the frames/ subdirectory were created on macOS with the command
```bash
ffmpeg -i qvmovie.mp4 -r 7 frame%d.png
```
which specifies a frame rate of 7 fps.  The files produced by the above command
are imported into the paper by the following LaTeX animate package command:
```latex
\animategraphics[width=0.85\columnwidth,controls,autoplay]{7}{figures/icar/frames/frame}{1}{30}
```
which displays frame1.png through frame30.png at 7 fps, launches the animation
automatically when the page is viewed, and adds control buttons play, rewind, etc.

Prerequisite: 
-------------
Acrobat Reader 7 or later is required for the animation to display in the resulting 
PDF document.

Known Issues
------------
* Apple Preview will not display the animation.
* LaTeX must run twice for Acrobat Reader to display the animation.
