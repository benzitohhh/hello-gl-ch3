This is the source code for the "hello world" OpenGL application described in
chapter 3 of Joe Groff's OpenGL tutorial: 

http://duriansoftware.com/joe/An-intro-to-modern-OpenGL.-Chapter-3:-3D-transformation-and-projection.html

This is also helpful:

https://en.wikibooks.org/wiki/OpenGL_Programming


## To install on OSX


### GLUT

On OSX, `GLUT` framework is already available,
located at `/System/Library/Frameworks/GLUT.framework`.

Note that many of the functions are now deprecated by Apple,
and these functions can cause compile warnings, and also
not show up in TAGS file.

Still, `man` pages are available for most of the functions
(i.e. `man glutInit`)

### GLEW

`GLEW` needs to be installed. So do `brew install glew`.
This installs the header files in `/usr/local/include/GL/`

To add a TAGS file for it:
```
cd /System/Library/Frameworks/GLUT.framework;
sudo ctags -e -R
```


### Building

```
make clean; make; ./hello-gl
```

### Running

Vertex shaders can be specified as an argument on the command line:
```
make; ./hello-gl naive-perspective-rotation.v.glsl
```


i.e. `Makefile` is a symlink to `Makefile.MacOSX`



## Note that GL matrices are column-major
i.e. inverted to how they are normally written in maths papers.




## Angle of View

https://en.wikipedia.org/wiki/Angle_of_view

Alpha in [0, pi/2].

Bigger angle (wider field of view) - further away items appear smaller (ZOOM OUT).

Smaller angle (narrower field of view) - further away items appear less different to nearer items (ZOOM IN).



## Viewing Frustrum

https://en.wikipedia.org/wiki/Viewing_frustum
