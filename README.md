# The Be Nice AMP Project

Building static HTML that is fast for the end user doesn't need to be hard. Just follow these simple instructions and I promise you that your site will be really fast.

The Be Nice AMP Project is entirely built on existing web technologies, there's no magic here. You can use HTML, Javascript, CSS and images. However: Never ever load Javascript synchronously. Just don't do it.

And make sure to inline the CSS inside of head if you use HTTP/1.1.

# How does the Be Nice AMP Project work on HTTP/1.1?

You need to build your HTML following this pattern.

```html
<!doctype html>
<html>
<head>
  <meta charset="utf-8">
  <link rel="canonical" href="hello-world.html" >
  <meta name="viewport" content="width=device-width,initial-scale=1,minimum-scale=1,maximum-scale=1,user-scalable=no,minimal-ui">
  <!-- Never ever load javascript asyncrounus, make sure you follow this pattern:
  <script src="https:/www./example.org/important.js" async></script>-->
  <style>body { background-color: yellow; }</style>
</head>
<body>Hello World!</body>
</html>
```

# How does the Be Nice AMP Project work on HTTP/2?
Are you lucky and already have upgraded to HTTP/2 and your server has the possibility to do a server push? Then make sure you push your CSS file and you don't even have to inline it in your HTML!

```html
<!doctype html>
<html>
<head>
  <meta charset="utf-8">
  <link rel="canonical" href="hello-world.html" >
  <meta name="viewport" content="width=device-width,initial-scale=1,minimum-scale=1,maximum-scale=1,user-scalable=no,minimal-ui">
  <!-- Never ever load javascript asyncrounus, make sure you follow this pattern:
  <script src="https:/www./example.org/important.js" async></script>-->
  <link rel="stylesheet" href="/css/general.css?1444300406"/>
</head>
<body>Hello World!</body>
</html>
```

## FAQ

 * [Question] Hmm, what? You don't even have to define the HTML with the ⚡ character, could this really be fast?

 Yes it is!

 * [Question] The Be Nice AMP Project doesn't come with a CDN, why?

 The cool thing with the Be Nice AMP Project is that it is compatible with your current CDN! You can just continue to use, just as before and your pages will be super fast.


## Be Nice AMP Project vs AMP HTML



# Who makes the Be Nice AMP Project?

Be Nice AMP Project is made by me [Peter](https://www.peterhedenskog.com), and is licensed
under the [Apache License, Version 2.0](LICENSE).

## Contributing

Please see [the CONTRIBUTING file](CONTRIBUTING.md) for information on contributing to the Be Nice AMP Project.
