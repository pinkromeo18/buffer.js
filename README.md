# buffer.js
#demo 
```
https://codepen.io/pinkromeo/pen/GRPaXMe
```
````
<script src="https://pinkromeo18.github.io/buffer.js/buffer.js"></script>
<input type="text" id="text" placeholder="original text">
<p id="encoded"></p>
<p id="decoded"></p>
````
````
document.querySelector('#text').addEventListener('input', () => {
  const txt = document.querySelector('#text').value;
  const encoded = buffer.Buffer.from(txt).toString('base64');
  document.querySelector('#encoded').innerText = encoded;
  const decoded = buffer.Buffer.from(encoded, 'base64').toString();
  document.querySelector('#decoded').innerText = decoded;
});
````
