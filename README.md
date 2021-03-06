<<<<<<< HEAD
**frontend-nanodegree-mobile-portfolio-project4**
**Frontend Project 4**
=======
## Website Performance Optimization portfolio project


**index.html** is the start page. From index.html you can reach Build Your Own 2048! What the hell is a 2048? as well as the Pizzeria page. 
PageSpeed Insights for **index.html** 
<ul>
	<li>Mobile: 95/100</li>
	<li>Desktop: 97/100</li>
</ul>
To achieve these scores I 
<ol>
	<li>Resized the image pizzaria.jpg from its original size of 2048 x 1536 to 100 x 75 px</li>
    <li>Added _meta http-equiv="Cache-Control" content="max-age=600"_ (although admittedly it did not seem to make a difference)</li>
    <li>Minified print.css (print_mini.css)</li>
    <li>Added media="print" to print_mini.css ref</li>
    <li>In-lined Smartphones (portrait) script</li>
    <li>Added async to script references</li>
    <li>In-lined cb and rf scripts</li>
 </ol>
 
 **pizza.html** achieve an FPS of 60 consistently when scrolling
 To achieve this I 
 <ol>
 	<li>Reduced the size of _pizza.png_ as well as optimized for web using Adobe Image Ready 7</li>
 	<li>Minified _main.js_</li>
 	<li>Reduced the number of pizzas created from the original 200 down to 35</li>
 	<li>Added _requestAnimationFrame_ to scrolling event listener</li>
 	<li>Took _(document.body.scrollTop / 1250)_ out of the _for_ loop in the _phase_ variable and assigned it to a new variable called _top_ and put it outside the _for_ loop</li>
 	<li>In the _i_ var I assigned the beginning count to the length of the 'mover' items then decremented instead incremented </li>
 	<li>Added _"translateX("+left+") translateZ(0)";_ to _updatePosition_ function instead of using _items_ array</li>
 	
 </ol>
 
 **pizza.html** achieve 5ms or less when changing pizza sizes on slider. 
 <ol>
 	<li>Moved _var dx_ outside the _for_ loop of _changePizzaSizes_ function</li>
 	<li>Moved _var newidth_ outside the _for_ loop of _changePizzaSizes_ function</li>
 	<li>Moved _document.querySelectorAll(".randomPizzaContainer")_ outside the _for_ loop and assigned it to a newly created variable array called _elements_</li>
 	<li>For _var i_ I assigned a beginning value of the _elements_ (randomPizzaContainer) variable instead of zero, as we will always have at least one. I then decremented</li>
 </ol>
 
 **Resources**
 <ul>
 	<li><a href="https://developer.chrome.com/devtools/docs/demos/too-much-layout/index">Google Timeline demo</a></li>
 	<li><a href="https://developers.google.com/speed/pagespeed/insights/?url=http%3A%2F%2Fcygnusx1z.github.io%2Ffrontend-nanodegree-mobile-portfolio-project4%2F&tab=mobile">PageSpeed Insights</a></li>
 	<li><a href="https://developer.chrome.com/devtools/docs/network">Evaluating network performance</a></li>
 	<li><a href="http://jscompress.com">jscompress.com</a></li>
 	<li><a href="http://jankfree.org/">jankfree</a></li>
 	<li><a href="http://www.smashingmagazine.com/2013/06/10/pinterest-paint-performance-case-study/">Gone In 60 Frames Per Second: A Pinterest Paint Performance Case Study</a></li>
 </ul>
 
 


=======
## Website Performance Optimization portfolio project

Your challenge, if you wish to accept it (and we sure hope you will), is to optimize this online portfolio for speed! In particular, optimize the critical rendering path and make this page render as quickly as possible by applying the techniques you've picked up in the [Critical Rendering Path course](https://www.udacity.com/course/ud884).

To get started, check out the repository, inspect the code,

### Getting started

Some useful tips to help you get started:

1. Check out the repository
1. To inspect the site on your phone, you can run a local server

  ```bash
  $> cd /path/to/your-project-folder
  $> python -m SimpleHTTPServer 8080
  ```

1. Open a browser and visit localhost:8080
1. Download and install [ngrok](https://ngrok.com/) to make your local server accessible remotely.

  ``` bash
  $> cd /path/to/your-project-folder
  $> ngrok 8080
  ```

1. Copy the public URL ngrok gives you and try running it through PageSpeed Insights! [More on integrating ngrok, Grunt and PageSpeed.](http://www.jamescryer.com/2014/06/12/grunt-pagespeed-and-ngrok-locally-testing/)

Profile, optimize, measure... and then lather, rinse, and repeat. Good luck!

### Optimization Tips and Tricks
* [Optimizing Performance](https://developers.google.com/web/fundamentals/performance/ "web performance")
* [Analyzing the Critical Rendering Path](https://developers.google.com/web/fundamentals/performance/critical-rendering-path/analyzing-crp.html "analyzing crp")
* [Optimizing the Critical Rendering Path](https://developers.google.com/web/fundamentals/performance/critical-rendering-path/optimizing-critical-rendering-path.html "optimize the crp!")
* [Avoiding Rendering Blocking CSS](https://developers.google.com/web/fundamentals/performance/critical-rendering-path/render-blocking-css.html "render blocking css")
* [Optimizing JavaScript](https://developers.google.com/web/fundamentals/performance/critical-rendering-path/adding-interactivity-with-javascript.html "javascript")
* [Measuring with Navigation Timing](https://developers.google.com/web/fundamentals/performance/critical-rendering-path/measure-crp.html "nav timing api"). We didn't cover the Navigation Timing API in the first two lessons but it's an incredibly useful tool for automated page profiling. I highly recommend reading.
* <a href="https://developers.google.com/web/fundamentals/performance/optimizing-content-efficiency/eliminate-downloads.html">The fewer the downloads, the better</a>
* <a href="https://developers.google.com/web/fundamentals/performance/optimizing-content-efficiency/optimize-encoding-and-transfer.html">Reduce the size of text</a>
* <a href="https://developers.google.com/web/fundamentals/performance/optimizing-content-efficiency/image-optimization.html">Optimize images</a>
* <a href="https://developers.google.com/web/fundamentals/performance/optimizing-content-efficiency/http-caching.html">HTTP caching</a>

### Customization with Bootstrap
The portfolio was built on Twitter's <a href="http://getbootstrap.com/">Bootstrap</a> framework. All custom styles are in `dist/css/portfolio.css` in the portfolio repo.

* <a href="http://getbootstrap.com/css/">Bootstrap's CSS Classes</a>
* <a href="http://getbootstrap.com/components/">Bootstrap's Components</a>

### Sample Portfolios

Feeling uninspired by the portfolio? Here's a list of cool portfolios I found after a few minutes of Googling.

* <a href="http://www.reddit.com/r/webdev/comments/280qkr/would_anybody_like_to_post_their_portfolio_site/">A great discussion about portfolios on reddit</a>
* <a href="http://ianlunn.co.uk/">http://ianlunn.co.uk/</a>
* <a href="http://www.adhamdannaway.com/portfolio">http://www.adhamdannaway.com/portfolio</a>
* <a href="http://www.timboelaars.nl/">http://www.timboelaars.nl/</a>
* <a href="http://futoryan.prosite.com/">http://futoryan.prosite.com/</a>
* <a href="http://playonpixels.prosite.com/21591/projects">http://playonpixels.prosite.com/21591/projects</a>
* <a href="http://colintrenter.prosite.com/">http://colintrenter.prosite.com/</a>
* <a href="http://calebmorris.prosite.com/">http://calebmorris.prosite.com/</a>
* <a href="http://www.cullywright.com/">http://www.cullywright.com/</a>
* <a href="http://yourjustlucky.com/">http://yourjustlucky.com/</a>
* <a href="http://nicoledominguez.com/portfolio/">http://nicoledominguez.com/portfolio/</a>
* <a href="http://www.roxannecook.com/">http://www.roxannecook.com/</a>
* <a href="http://www.84colors.com/portfolio.html">http://www.84colors.com/portfolio.html</a>
>>>>>>> refs/remotes/origin/master
