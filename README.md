# Welcome to the MathVision repository

**Create, by means of a math formula, static, animated, and interactive 2D images.**

MathVision.html aims at allowing you, the user, to **focus on the math formula and user interaction**, and, after a few minutes of training, obtain cool and exciting results.

* MathVision.html entirely runs in your browser. Follow [this link](http://htmlpreview.github.io/?https://github.com/pbauermeister/MathVision/blob/master/MathVision.html).

* Gallery of results: http://www.openprocessing.org/user/35108

* Comprehensible step-by-step tutorial: http://www.instructables.com/id/MathVision/.

MathVision.html is inspired by and dedicated to the Amiga MathVISION software, see http://home.olympus.net/~7seas/. 


## Features

* **Contour plot**: Static images are computed by a parametric formula:
> color(x, y) = rgb(u, v)

  where u and v are two parameters mapped onto the two dimensions [x,y] of a canvas. 

* **Animated plot**: The pictures can be animated by including a 3rd parameter, the time:
> color(x, y, t) = rgb(u, v, t) 

* **User interactivity**: Accessing the mouse coordinates allows to make the pictures interactive. 

* **Color model**: rgb and hsb models are both supported. 

## How it Works

MathVision.html involves a combination of the following technologies.

### HTML5 Canvas

All (graphics, animation, user interaction) is completely handled by your HTML5 enabled web browser. There is no Flash involved here.

The 2D mode of the <canvas> element is used and controlled by some auto-generated JavaScript.

About HTML5 canvas, see http://www.html5canvastutorials.com/tutorials/html5-canvas-tutorials-introduction/.

### Processing.js

Wikipedia says: Processing.js is a JavaScript port of Processing, a programming language designed to write visualizations, images, and interactive content. It allows web browsers to display animations, visual applications, games and other graphical rich content without the need for a Java applet or Flash plugin.

This project could have been done without Processing.js, but the latter brings a very nice programming model,
providing a quite rich API, which is also portable (small effort would be required to port the project on other, non-web, implementations pf Processing). 

(In fact, this project was motivated by the wish to learn Processing.) 

See: http://processingjs.org/

### Your HTML5 enabled web browser

When your browser encounters the first <script> tag, it will fetch the Processing.js implementation script, which is just a big JavaScript program.

Then, when encountering the second <script> tag, it will pass its content to the fetched processing.js script. The content is, well, processed by processing.js, which turns the content into JavaScript code that your browser can execute.

Finally, this generated JavaScript run and applied to the <canvas> element.
