# Blu
Something I made dont even know.
What this is just and easier to add events to elements. Example

```html
<html>
	<head>
		<link rel="stylesheet" href="test.css">
	</head>
	<body>
		<div id="app">
			<div class="nav">
				<a href="#" class="linke">Home</a>
				<a href="#" class="linke">About</a>
				<a href="#" class="linke">Contact</a>
				<a href="#" class="linke">Projects</a>
			</div>
			<button id="button" b-on:click="hello">Hit</button>
		</div>
	</body>
	<script type="module" src="main.js"></script>
</html>

```
As you can see the button element has the b-on attribute and right after that the event you want to listen and in the quotes you put the name of the function you want to call when this event is fired.

Note:
You put this attribute on elements that you want to register an event for

Now that you have the attribute on your desired element lets get to the Javascript you need to make this work

```javascript
var button = new Blu("button", {
	hello: function(){
		console.log("Hello World from the button2 event")
	}
})
```
All you have to do to register the event now is make an instance of the Blu constructor.You first pass in the id of the element(It has to be an ID cant be anything else) then you pass in an object with the methods this element can use.Once you do this your element should be registered and the hello function will be called when the button is clicked.
