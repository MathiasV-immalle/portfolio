# HTML
## Part 2: Canvas
- canvas

`<canvas>` element creates a canvas.
```
<canvas id="canvas1" width="200" height="100">
</canvas>
```
- script

The `<canvas>` element must have an id attribute so it can be referred to by JavaScript.
```
<script>
     var can = document.getElementById("canvas1");
     var ctx = can.getContext("2d");
  </script>
```
- fillRect

The `fillRect(x, y, w, h)` method draws a "filled" rectangle, in which `w` indicates width and `h` indicates height. The default fill color is black. 
```
var c=document.getElementById("canvas1");
var ctx=c.getContext("2d");
ctx.fillRect(20,20,100,100);
```
- fillStyle

The `fillStyle` property is used to set a color, gradient, or pattern to fill the drawing.
Using this property allows you to draw a green-filled rectangle.
```
ctx.fillStyle ="rgba(0, 200, 0, 1)";
```
- Draw a Line

`moveTo(x,y)`: Defines the starting point of the line.
`lineTo(x,y)`: Defines the ending point of the line.

- Draw a Circle

`beginPath()`: Starts the drawing.
`arc(x,y,r,start,stop)`: Sets the parameters of the circle.
`stroke()`: Ends the drawing.

- Gradients

`createLinearGradient(x,y,x1,y1)`: Creates a linear gradient.
`createRadialGradient(x,y,r,x1,y1,r1)`: Creates a radial/circular gradient.

- Drawing Text on the Canvas

`Font`: Defines the font properties for the text.
`fillText(text,x,y)`: Draws "filled" text on the canvas.
`strokeText(text,x,y)`: Draws text on the canvas (no fill).
`ctx.translate(100, 150)`: Sets new x and y for the canvas
`ctx.fillText("after translate", 10, 30)`: Sets new x and y for text in canvas
`ctx.rotate( (Math.PI / 180) * 25)`: Rotates 25 degrees. -> in RADIANS
`ctx.scale(1.5, 4)`: Scales the canvas 1.5 times in the X-direction, and 4 times in Y-direction

### You still want to learn more? Feel free to visit Part 3 [HERE](Web-storage-objects+Geolocation.md)
