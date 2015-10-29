[![Circle CI](https://circleci.com/gh/tmcw/big/tree/gh-pages.svg?style=svg&circle-token=2963848e42fe67b8a66a2ad2d6dd99d05bdde6a4)](https://circleci.com/gh/tmcw/big/tree/gh-pages)

This is a ridiculous presentation system that works great for
creative, hurried people. See [the demo](http://macwright.org/big/demo.html)
for an example of it working.

It makes text and images as big as they can be, gives you minimal
styling (`em`) and keyboard controls for navigation.

## Quickstart

You can skip every step by doing

    wget https://raw.github.com/tmcw/big/gh-pages/big.quickstart.html

This is a **bundle of all JS, CSS, and HTML code** - which means that it's
a bit harder to update, but there are **no external dependencies** here,
so no conference-wifi-pwn.

### Launch locally

Serve locally via:

```
python -m SimpleHTTPServer
```


## Slowstart

big makes sense if you're comfortable with JavaScript, CSS, and HTML.
If you are very familiar with those languages, you can jump right in.
Otherwise, here are some tips:

* When you are working locally you can view your slides by opening your
  presentation in a browser. Remember to save the file as a `.html`.
* Use `<div>` & `</div>` around each slide
* You may be used to `em` displaying as italicized text, but in big emphasized
  text is green and unitalicized. You can change this default behavior in the header. <em>(Look, Ma-- CSS in action!)</em>
* Paragraph tags aren't displayed in big. This can be a useful place for you
  to store your speaking notes. (I don't actually understand this, but I've seen it done)
* If you'll have internet access when you present, you can reference images
  hosted online. If you won't, any images you want to reference will need to
  be in the same folder as your presentation.

## Examples

A full presentation looks like:

```html
<!DOCTYPE html>
<html>
<head>
  <title>Big</title>
  <meta charset='utf-8'>
  <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=0" />
  <link href='big.css' rel='stylesheet' type='text/css' />
  <script src='big.js'></script>
</head>
<body>
<div>use &harr; to navigate</div>
<div>Big</div>
<div class="center"><em>Presentation software</em> for busy busy hackers</div>
<div>+text</div>
<div>as <em>big</em> as it can be</div>
<div data-time-to-next="3">and now it's perfect for ignite talks (wait 3 seconds)</div>
<div>no config</div>
<div><em>1.5k</em></div>
<div><img src='http://farm3.static.flickr.com/2506/5757000880_509440308e_z.jpg' /> images too</div>
<div data-bodyclass="new-shiny">per slide body classes</div>
<div>JS+CSS <a href='https://github.com/tmcw/big'>github.com/ tmcw/ big</a></div>
</body>
</html>
```

Here's how you write a single slide

```html
<div>Hello, I am a slide</div>
```

A slide that automatically advances in 5 seconds

```html
<div data-time-to-next='5'>Life is short but sweet for certain</div>
```

A slide that changes the body tag's class to 'minard'

```html
<div data-bodyclass='minard'>Winter sucks</div>
```
