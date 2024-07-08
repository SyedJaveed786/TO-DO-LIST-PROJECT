### Project Assignment: Build a To-Do List Application Using 
### ES6 JavaScript

```
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Document</title>
<link
href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css"
rel="stylesheet" integrity="sha384-
QWTKZyjpPEjISv5WaRU9OFeRpok6YctnYmDr5pNlyT2bRjXh0JMhjY6hW+ALEwIH"
crossorigin="anonymous">
<link href="https://cdn.jsdelivr.net/npm/bootstrap-icons/font/bootstrapicons.css" rel="stylesheet">
<script
src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/js/bootstrap.bundle.min
.js" integrity="sha384-
YvpcrYf0tY3lHB60NNkmXc5s9fDVZLESaAA55NDzOxhy9GkcIdslK1eN7N6jIeHz"
crossorigin="anonymous"></script>
<style>
li {
list-style-type: none;
border-radius: 20px;
height: 40px;
margin: 10px;
padding-left: 20px;
font-size: 20px;
background-color: aliceblue;
position: relative;
}
li .bi-trash {
position: absolute;
right: 40px;
color: red;
cursor: pointer;
}
.st {
text-decoration: line-through;
}
.bi-x-circle {
font-size: 20px;
color: red;
cursor: pointer;
margin-left: 10px;
}
</style>
</head>
<body>
<div class="card mx-auto" style="width: 30rem; padding-bottom: 20px;">
<div class="card-header bg-success text-white text-center">
<h1>Works to-dos</h1>
</div>
<div class="card-body text-center">
<p>Enter text into the input field to add items to your list.</p>
<p>Click the item to mark it as complete.</p>
<p>Click the "X" to remove the item from your list.</p>
<p>Add Task: <input type="text" name="name" id="txttask"
style="border: solid 2px; border-radius: 20px;">
<button class="btn btn-primary" style="border-radius: 20px;"
id="addtask">Add</button>
<i class="bi bi-x-circle" id="cleartasks"></i>
</p>
<ul id="container"></ul>
</div>
</div>
<script>
document.addEventListener('DOMContentLoaded', function() {
document.getElementById('container').addEventListener('click', 
function(event) {
if (event.target.tagName === 'SPAN') {
event.target.classList.toggle('st');
} else if (event.target.classList.contains('bi-trash')) {
event.target.parentElement.remove();
}
});
document.getElementById('addtask').addEventListener('click', 
function() {
var taskText = document.getElementById('txttask').value;
if (taskText) {
var li = document.createElement('li');
var span = document.createElement('span');
span.textContent = taskText;
var trashIcon = document.createElement('i');
trashIcon.classList.add('bi', 'bi-trash');
li.appendChild(span);
li.appendChild(trashIcon);
document.getElementById('container').appendChild(li);
document.getElementById('txttask').value = ''; // Clear 
the input field after adding the task
}
});
document.getElementById('cleartasks').addEventListener('click', 
function() {
document.getElementById('container').innerHTML = '';
});
});
</script>

### OUTPUT:
![Screenshot 2024-07-08 215429](https://github.com/SyedJaveed786/TO-DO-LIST-PROJECT/assets/106874713/81b914d5-40fe-4410-a33b-d01e8b5d30f8)

</body>
</html>
```
