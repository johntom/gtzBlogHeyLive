title: Adding Swiper to Corporate Theme
date: 2016-07-31 10:24:41
tags:
author:
---
#### adding swiper
Just descovered hexo.io on July 27th and tooling around learned how to add libs

Swiper is an awesome slide contoller check it out
[http://idangero.us/swiper/#.V54KlegrKUk]()

on github

[https://github.com/nolimits4web/Swiper]()


##### Adding swiper to the awesome hexo.io Corporate theme
https://github.com/ptsteadman/hexo-theme-corporate

- add swiper.min.js to \themes\corporate\source\js\swiper.min.js
- modify \themes\corporate\layout\_partial\scripts.ejs

<pre>
<%- js('js/swiper.min.js') %>

&lt;Script type="text/javascript" &gt;
    jQuery(document).ready(function() {
        Layout.init();    
        Layout.initOWL();
        Layout.initTwitter();
        Layout.initFixHeaderWithPreHeader(); /* Switch On Header Fixing (only if you have pre-header) */
        Layout.initNavScrolling(); 
	new WOW().init();
    var swiper = new Swiper('.swiper-container');
 
    });&lt;/Script&gt;
</pre>


<pre>
Now add it to a dirrectory in \source\dirname\index.ejs
---
title: Swiper
date: 2015-11-17 01:00:51
layout: page
---
    &lt;link rel="stylesheet" href="./swiper.min.css">
    &lt;!-- Demo styles -->
    &lt;style>
    body {
        background: #eee;
        font-family: Helvetica Neue, Helvetica, Arial, sans-serif;
        font-size: 14px;
        color:#000;
        margin: 0;
        padding: 0;
    }
    .swiper-container {
        width: 500px;
        height: 300px;
        margin: 20px auto;
    }
    .swiper-slide {
        text-align: center;
        font-size: 18px;
        background: #fff;
        
        /* Center slide text vertically */
        display: -webkit-box;
        display: -ms-flexbox;
        display: -webkit-flex;
        display: flex;
        -webkit-box-pack: center;
        -ms-flex-pack: center;
        -webkit-justify-content: center;
        justify-content: center;
        -webkit-box-align: center;
        -ms-flex-align: center;
        -webkit-align-items: center;
        align-items: center;
    }
    &lt;/style>
    &lt;!-- Swiper -->
    &lt;div class="swiper-container">
        &lt;div class="swiper-wrapper">
            &lt;div class="swiper-slide">Slide 1&lt;/div>
            &lt;div class="swiper-slide">Slide 2&lt;/div>
            &lt;div class="swiper-slide">Slide 3&lt;/div>
            &lt;div class="swiper-slide">Slide 4&lt;/div>
            &lt;div class="swiper-slide">Slide 5&lt;/div>
            &lt;div class="swiper-slide">Slide 6&lt;/div>
            &lt;div class="swiper-slide">Slide 7&lt;/div>
            &lt;div class="swiper-slide">Slide 8&lt;/div>
            &lt;div class="swiper-slide">Slide 9&lt;/div>
            &lt;div class="swiper-slide">Slide 10&lt;/div>
        &lt;/div>
    &lt;/div>
</pre>