# HTML
## Part 1: The beginning 
- article

`<article>` is a self-contained, independent piece of content that can be used and distributed separately from the rest of the page or site.
```
<article>
	<h1>The article title</h1>
	<p>Contents of the article element</p>
</article>
```
- section 

`<section>` is a logical container of the page or article. 
Sections can be used to divide up content within an article. 
```
<article>
	<h1>The article title</h1>
	<p>Contents of the article element</p>
	<section>
		<h1>Heading</h1>
		<p>content or image</p>
</section>
</article>
```
- aside 

`<aside>` is secondary or tangential content which could be considered separate from but indirectly related to the main content.
```
<article>
	<h1>The article title</h1>
	<p>Contents of the article element</p>
	<aside>
		<p>Element</p>
	</aside>
</article>
```
- audio 

`<audio>` element specifies a standard for embedding audio in a web page.
```
<audio src="audio.mp3" controls>
Audio element not supported by your browser
</audio>
```
Currently, there are three supported file formats for the <audio> element: MP3, WAV, and OGG.
- audiocontrols 
```
<audio controls>
<source src="audio.mp3" type="audio/mpeg">
<source src="audio.ogg" type="audio/ogg">
Audio element not supported by your browser
</audio>
```
- autoplay 

`<autoplay>`
When this attribute is defined, audio starts playing as soon as it is ready, without asking for the visitor's permission.
```
<audio controls autoplay>
```
- loop 

`<loop>`
This attribute is used to have the audio replay every time it is finished.
```
<audio controls loop>
```
- video 

`<video>` element is similar to the audio element. 
```
<video controls>
<source src="video.mp4" type="video/mp4">
  	<source src="video.ogg" type="video/ogg">
  	Video is not supported by your browser
</video>
```
autoplay and loops also works here.
- progress 
 
`<progress>` element provides the ability to create progress bars on the web.
```
<progress>
Status: <progress min="0" max="100" value="35">
</progress>
```
Value: Specifies how much of the task has been completed. 
Max: Specifies how much work the task requires in total.
- animate 

`<animate>` element makes us able to create SVG animations.
```
<svg width="1000" height="250">
<rect width="150" height="150" fill="orange">
<animate attributeName="x" from="0" to="300"
   		dur="3s" fill="freeze" repeatCount="2"/>
</rect>
</svg>
```
- path 

`<path>` element is used to define a path.

M: moveto
L: lineto
H: horizontal lineto
V: vertical lineto
C: curveto
S: smooth curveto
Q: quadratic Bézier curve
T: smooth quadratic Bézier curveto
A: elliptical Arc
Z: closepath
```
<svg width="500" height="500">
<path d="M 0 0 L200 200 L200 0 Z" style="stroke:#000;  fill:none;" />
</svg>
```
M places our "virtual pen" down at the position 0, 0. It then moves 200px down and to the right, then moves up to the position 200, 0. The Z command closes the shape, which results in a triangle.
- form 

`<form>` element.
```
<form autocomplete=”off”>
<label>Your name:</label>
<input id="user" name="username" type="text" placeholder=”email@example.com” autofocus required/>
</form>
```
- autocomplete 

`<autocomplete>` attribute makes that the required field is not filled in automatically with info based on values that the user has entered before. 


- placeholder 

`<placeholder>` attribute provides a hint to the user of what information can be entered into the field.

- autofocus 

`<autofocus>` attribute makes the desired input focus when the form loads.
- required

`<required>` attribute makes that the form will not be submitted without filling in the required fields.

### You still want to learn more? Feel free to visit Part 2 [HERE](Canvas.md)
