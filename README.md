# The Be Nice AMP Project

Building static HTML that is fast for the end user doesn't need to be hard. Just follow these simple instructions and I promise you that your site will be really fast.

The Be Nice AMP Project is entirely built on existing web technologies and best practices, there's no magic here. You can use HTML, Javascript, CSS and images. However: Never ever load Javascript synchronously. Just don't do it.

And make sure to inline the CSS inside of head if you use HTTP/1.1.

Want to see the Be Nice project in action? Read the [blog post](https://www.peterhedenskog.com/blog/2015/10/the-be-nice-approach-to-mobile-and-web-performance/)! Do you want to know what is faster: The Be Nice project or the AMP Project? Checkout the results testing using 2GFast emulated mobile http://www.webpagetest.org/video/compare.php?tests=151013_7D_KMK,151013_A4_KM7

# How does the Be Nice AMP Project work on HTTP/1.1?

You need to build your HTML following this pattern.

```html
<!doctype html>
<html>
<head>
  <meta charset="utf-8">
  <link rel="canonical" href="hello-world.html" >
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <!-- Never ever load javascript synchronous, make sure you follow this pattern:
  <script src="https://www.example.org/important.js" async></script>-->
  <style>body { background-color: yellow; }</style>
</head>
<body>Hello World!</body>
</html>
```

If you have lots and lots of CSS and you feel that inlining it will be kind of bad, have a look at [loadCSS](https://github.com/filamentgroup/loadCSS) project by the Filament Group.

# How does the Be Nice AMP Project work on HTTP/2?
Are you lucky and already have upgraded to HTTP/2 and your server has the possibility to do a server push? Then make sure you push your CSS file and you don't even have to inline it in your HTML!

```html
<!doctype html>
<html>
<head>
  <meta charset="utf-8">
  <link rel="canonical" href="hello-world.html" >
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <!-- Never ever load javascript synchronous, make sure you follow this pattern:
  <script src="https:/www./example.org/important.js" async></script>-->
  <link rel="stylesheet" href="/css/general.css?1444300406"/>
</head>
<body>Hello World!</body>
</html>
```

## FAQ

 * **Question:** Hmm, what? You don't even have to define the HTML with the ⚡ character, could this really be fast?

 Yes it is! Try it out and you will see.

 * **Question:** The Be Nice AMP Project doesn't come with a CDN, why?

 The cool thing with the Be Nice AMP Project is that it is compatible with your current CDN! You can just continue to use it and your pages will be super fast.

 * **Question:** Joining the AMP Project will make my pages rank higher in Google. Can you promise the same with the *Be Nice AMP Project*? 
 
  No, sorry.

 * **Question:** The AMP Project has some new cool tags like *amp-img* instead of using the old classic img tag. Is this something I can use in the Be Nice project?
 
 No, we don't support these tags out of the box. But we have kind of a cool feature where you can load whatever javascript you want, so you free to build it.

## Be Nice AMP Project vs AMP HTML
You probably heard of the Google project [AMP Project](https://github.com/ampproject/amphtml) that is kind of the same thing as the Be Nice AMP Project except for a couple of things:

* The AMP project have *"A new approach to web performance"* making your website dependent on Google. The Be Nice AMP Project follow the old approach: Make your site fast following best practice guidelines and be independent of Google.

* With the *Be Nice AMP Project* you don't have to define your HTML tag with the ⚡ character like ```<html ⚡>```. It will still be fast!

# Who makes the Be Nice AMP Project?

Be Nice AMP Project is made by me [Peter](https://www.peterhedenskog.com), and is licensed
under the [Apache License, Version 2.0](LICENSE).

## Contributing

Please see [the CONTRIBUTING file](CONTRIBUTING.md) for information on contributing to the Be Nice AMP Project.
