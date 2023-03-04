# GeneratedArt-circle

This is a Processing code that draws a noise-based circular shape that changes over time. Here is an explanation of the code:

- float resolution = 260;: This sets the number of points to use when drawing the circle.
- float rad = 100;: This sets the radius of the circle.
- float x = 1;: This sets the x-coordinate of the current point being drawn.
- float y = 1;: This sets the y-coordinate of the current point being drawn.
- float t = 255;: This sets the starting value of the time variable.
- float tChange = .10;: This sets how much the time value changes each frame.
- float nVal;: This variable will hold the noise value for each point.
- float nInt = 3;: This sets the intensity of the noise function.
- float nAmp = 3;: This sets the amplitude of the noise function.
- boolean filled = true;: This variable determines whether the shape is filled or not.

The setup() function is run once at the start of the program. It sets the size of the canvas and the level of detail for the noise function.

The draw() function is run repeatedly to create each frame of the animation. It first sets the background to white and then translates the coordinate system to the center of the canvas. If the filled variable is true, it draws a filled red circle in the top right corner. Otherwise, it sets the stroke to black with a thickness of 10.

The nInt and nAmp variables are updated based on the mouse position. They are then used to calculate the noise value for each point on the circle. The noise value is mapped to a range of nAmp to 1, so that the points closer to the center of the circle have a smaller amplitude than those further away.

The x and y coordinates of each point on the circle are calculated using trigonometry and the noise value. Finally, the point is added to the shape being drawn using the vertex() function. The shape is closed using the endShape(CLOSE) function.

The mouseClicked() function is called whenever the mouse is clicked. It toggles the value of filled, which determines whether the shape is filled or not.
