# Ghost EXP+1 / Code Highlighting

I love code, so i often want to share some. But using the default Casper theme, the styling of code blocks is pretty basic - no syntax highlighting. It was great to see how simple Ghost could be extended to support syntax highlighting using [highlight.js](https://highlightjs.org).

Just put the following lines in the "Code Injection" / "Blog Header" section of your Ghost settings and you are ready to go. 

```
<link rel="stylesheet" type="text/css" href="https://cdnjs.cloudflare.com/ajax/libs/highlight.js/9.3.0/styles/hybrid.min.css">
<script src="https://cdnjs.cloudflare.com/ajax/libs/highlight.js/9.3.0/highlight.min.js"></script>  
<script>hljs.initHighlightingOnLoad();</script>
<style>
/* evil hack to prevent linebreaks */
.hljs { width: 2300px; }
pre { padding: 0px; border-radius: 10px; }
</style>
```

The gigantic width set in the CSS is an evil hack i found [here](http://stackoverflow.com/a/34644091/1010496) to prevent linebreaks. If you like your code to be cut into pieces, you can safely ignore the style block. The language will be determined by highlight.js automagically, but you can also set it explicitly using pre- and code-tags.

```
<pre><code class="cs">
// my fancy c# code here
private Func<int, int> _inc = (i) => { return i + 1; }  
<∕code><∕pre>
```

Finally if you want to have a look at all available color themes visit the demo page [here](https://highlightjs.org/static/demo). And in case you are looking for line numbers, you are [officially](http://highlightjs.readthedocs.io/en/latest/line-numbers.html) out of luck ¯\\\_(ツ)_/¯

Enjoy! :)