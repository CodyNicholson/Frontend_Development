# Loading Images Into Canvas

```html
<!DOCTYPE html>
<html>
<head>
	<title>Canvas Test</title>
</head>
<body>
	<canvas id="c" width="400" height="200"></canvas>
	<script type="text/javascript">
		var c = document.querySelector("#c");
		var ctx = c.getContext("2d");

		var image = new Image();

		image.onload = function() {
			console.log("Loaded image");
			ctx.drawImage(image, 0, 0, c.width, c.height);
		}

		image.src = "img.png";
	</script>
</body>
</html>
```

First, we create an empty canvas in the body of our html document

Then we write javaScript code that will get the canvas and the canvas's context

After our we have the context of our canvas we can call onLoad() on our image and pass it a function that will print a message to the console and draw the image in our canvas
