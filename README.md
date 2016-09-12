# scroll-down-anchor
Adding a scroll down anchor button to your website makes it easier for users to navigate through your website without having to manually scroll. In this tutorial, [Solodev](https://www.solodev.com/) provides you with the code you need to add an anchor button to your website and the JavaScript to enable scroll down functionality when the button is clicked.

## Tutorial

For detailed instructions, view Solodev's [Adding a Scroll Down Anchor Button to your Website](https://www.solodev.com/blog/web-design/adding-a-scroll-down-anchor-button-to-your-website.stml) article.

## Demo

Check out a working example on [JSFiddle](https://jsfiddle.net/solodev/3stm0mnq/).

## HTML

The scroll down anchor contains the following basic HTML markup.

```
<section class="company-heading intro-type" id="parallax-one">
   <div class="container">
      <div class="row product-title-info">
         <div class="col-md-12">
            <h1>
               DATA. DATA. DATA.
            </h1>
            <a class="ct-btn-scroll ct-js-btn-scroll" href="#section2"><img alt="Arrow Down Icon" src="images/arrow-down-1.png"></a>
         </div>
      </div>
   </div>
   <div class="parallax" id="parallax-cta" style="background-image:url(https://www.solodev.com/assets/anchor/company-hero2.jpg);">
      &nbsp;
   </div>
</section>
<div class="main">
   <section id="section2">
      <div class="container jumbo">
         <div class="jumbotron">
            <h2>Let Big Data Change the Game</h2>
            <p>WebCorpCo is all about making sure your marketing stack is in alignment with your company as well as the customers you serve. There is no 'one size fits all' approach to marketing. Every business is unique, customers are unique, and your marketing should be as well.</p>
            <p><a class="btn btn-primary btn-lg" href="#" role="button">Learn more</a></p>
         </div>
   </section>
   </div>
</div>
```

## JavaScript

The following JavaScript is required to initialize the anchor.

```
$(document).ready(function(){
  $("a").on('click', function(event) {
    if (this.hash !== "") {
      event.preventDefault();
      var hash = this.hash;
      $('html, body').animate({
        scrollTop: $(hash).offset().top
      }, 800, function(){
        window.location.hash = hash;
      });
    } 
  });
});
```

## CSS

All necessary CSS is included in scroll-down.css

## External Includes

This tutorial includes the following third party resources.

```
<link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.7/css/bootstrap.min.css">
<link rel="stylesheet" href="scroll-down.css">
<script src="https://ajax.googleapis.com/ajax/libs/jquery/1.12.4/jquery.min.js"></script>
<script src="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.7/js/bootstrap.min.js"></script>
```
