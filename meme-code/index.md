# Meme code

Let's finish the meme generator off. Start from here: [https://trinket.io/html/1e318505af](https://trinket.io/html/1e318505af)

## Adding a form

You can copy and paste the HTML code below so it is just before your `<div>` elements:

```
<form>
Select a picture <input type="text" id="picture" onchange="update_image()">
<p>
Meme text: <input type="text" id="meme_text" oninput="update_text()" maxlength="70">
<p>
</form>
<p/>
```

This provides a text box where you can paste a link to an image, and a textbox where you can type the caption for your meme.

## Making it dynamic

Add the following code just above the closing `</body>` tag near the end of the document:

```
<script type="text/javascript">

// Update image onto the screen
function update_image(){
	var img = document.querySelector('img'); // Returns the first img element
	img.src =  document.getElementById("picture").value;
}

// Write the text onto the meme
function update_text(){
	document.getElementById("message").innerHTML = document.getElementById("meme_text").value;
}

</script>
```

Remove `skeleton.jpg` from the `<img>` tag, and remove my text from the `<div id="message">` tag.

Can you explain how this code works? Talk to your shoulder partner to see if you agree on how the code works. Hint: you will need to 

## Saved work from last time:

[Rex (1): https://trinket.io/html/7ba068dcec](https://trinket.io/html/7ba068dcec)

[Rex (2): https://trinket.io/html/d43f5ad28a](https://trinket.io/html/d43f5ad28a)

[Adam (1): https://trinket.io/html/6b86d23947](https://trinket.io/html/6b86d23947)

[Adam (2): https://trinket.io/html/76f2d1e3ea](https://trinket.io/html/76f2d1e3ea)

[Hans (1): https://trinket.io/html/98057d5f31](https://trinket.io/html/98057d5f31)

[Hans (2): https://trinket.io/html/04804e0468](https://trinket.io/html/04804e0468)

[Ezra: https://trinket.io/html/faa52c855d](https://trinket.io/html/faa52c855d)

[Olivere: https://trinket.io/html/ec4d4fb8c7](https://trinket.io/html/ec4d4fb8c7)

[Freddie: https://trinket.io/html/eb56619db8](https://trinket.io/html/eb56619db8)

[Hermione: https://trinket.io/html/49b4108d9a](https://trinket.io/html/49b4108d9a)


### Try this!

Try changing the `src=""` attribute on the `<img>` tag. You can find images using Google images, and right-click and choose `Copy Link`. You can then right-click and choose paste to add the URL
to your code.


## Full Solution

HTML:

```
<html>
<head>
<title>Meme Generator</title>
<link rel="stylesheet" href="style.css">
</head>
<body>

<form>
Select a picture <input type="text" id="picture" onchange="update_image()">
<p>
Meme text: <input type="text" id="meme_text" oninput="update_text()" maxlength="70">
<p>
</form>

<p>

<div id="message">&nbsp;</div>
<div id="image"><img src="" height="500" width="600"></div>


<script type="text/javascript">

// Update image onto the screen
function update_image(){
	var img = document.querySelector('img'); // Returns the first img element
	img.src =  document.getElementById("picture").value;
}

// Write the text onto the meme
function update_text(){
	document.getElementById("message").innerHTML = document.getElementById("meme_text").value;
}

</script>

</body>
</html>
```

CSS:

```
#message {
	background-color: transparent;
	font-size: 34px;
	font-family: "Impact";
	color: white;
	text-shadow: black 0px 0px 10px;
	width: 600px;
	position: absolute;
	left: 15px;
	top: 470px;
}

#image {
	width: 600px;
	border: 3px solid #000000;
}
```
