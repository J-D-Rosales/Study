<span style="color:yellow">IDEA:</span>
You can running putting a 
```html
<script>
// code from js
</script>
```
If you want to modularize your code, putting the js in another section o part, then:
use
```js
<script src="/path/to/script.js"></script>
```
You can also provide relative paths such as . /script.js
<span style="color:yellow">Evidencia:</span>

If `src` is set, the script content is ignored.

A single `<script>` tag can’t have both the `src` attribute and code inside.

This won’t work:

```markup
<script src="file.js">
  alert(1); // the content is ignored, because src is set
</script>
```

We must choose either an external `<script src="…">` or a regular `<script>` with code.

The example above can be split into two scripts to work:

```markup
<script src="file.js"></script>
<script>
  alert(1);
</script>
```

**Tags:**

**Referencias**:
[[Learn JavaScript Ultimate]]
## Brújula
<span style="color:	#87CEEB">West: Similar</span> 
Supplementary tools (anecdotes, quotes, scientific studies)

Related concepts
x
<span style="color:	#87CEEB">East: Opposite</span>
x

<span style="color:	#87CEEB">North: Theme Question</span>
x

<span style="color:	#87CEEB">South: What does this lead to</span>
x
