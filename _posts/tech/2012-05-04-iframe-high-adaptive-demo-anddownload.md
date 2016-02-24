---
layout: post
title: iframe高度自适应demo及下载
category: 技术
date: 2012-05-04 16:34:19
tags: iframe
---


1. 下载代码
	[jquery-auto-iframe-height](http://www.lost-in-code.com/programming/jquery-auto-iframe-height/)
或者 [下载](http://lnmp100.b0.upaiyun.com/2012/05/house9-jquery-iframe-auto-height-207b678-1.zip) 

2. 使用demo 
    
    ```
    <!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN" "http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd">
    <html xmlns="http://www.w3.org/1999/xhtml" xml:lang="en" lang="en">
      <head>
        <meta http-equiv="content-type" content="text/html; charset=utf-8" />
        <title>jQuery » iFrame Sizing</title>
        <link rel="stylesheet" type="text/css" media="all" href="css/master.css" />
        <script type="text/javascript" src="js/jquery-1.4.3.min.js"></script>
        <script type="text/javascript" src="js/jquery.iframe-auto-height.plugin.js"></script>
      </head>
      <body>
        <div id="container">
            <h1>
                jQuery » iFrame Sizing
            </h1>
            <p>
                This demo uses <a href="http://jquery.com/">jQuery</a> to dynamically size iframes based on content height.
                Original code by Nathan Smith, see <a href="http://sonspring.com/journal/jquery-iframe-sizing">original article</a>.
            </p>
            <p>
                Now a jquery plugin, download from github <a href="http://github.com/house9/jquery-iframe-auto-height">http://github.com/house9/jquery-iframe-auto-height</a>
                and view the README file.
            </p>
            <p>
              Best viewed locally with Firefox.
               | 
              <a href="index2.html">index2</a>
               | 
              <a href="index_with_tables.html">index_with_tables</a>
            </p>
    
            <iframe src="panoramic.html" class="photo" scrolling="no" frameborder="0"></iframe>
    
            <iframe src="iframe_1.html" class="column" scrolling="no" frameborder="0"></iframe>
            <iframe src="iframe_1.html" class="column" scrolling="no" frameborder="0"></iframe>
            <iframe src="iframe_1.html" class="column" scrolling="no" frameborder="0"></iframe>
            <iframe src="iframe_1.html" class="column" scrolling="no" frameborder="0"></iframe>
    
            <div class="clear"> </div>
    
            <iframe src="iframe_2.html" class="column" scrolling="no" frameborder="0"></iframe>
            <iframe src="iframe_2.html" class="column" scrolling="no" frameborder="0"></iframe>
            <iframe src="iframe_2.html" class="column" scrolling="no" frameborder="0"></iframe>
            <iframe src="iframe_2.html" class="column" scrolling="no" frameborder="0"></iframe>
    
            <div class="clear"> </div>
        </div>
        <!-- end #container -->
    
        <script type="text/javascript">
          // match all iframes / use jQuery or alias $
          jQuery('iframe').iframeAutoHeight();
    
          // only panoramic.html iframe with some extra height
          // $('iframe.photo').iframeAutoHeight({heightOffset: 50});
    
          // NOTES: you can wrap this in document ready if you like
          // but IE8 didn't always like it
        </script>
    
        <!--
        on chrome on mac get this error when viewing locally
        Unsafe JavaScript attempt to access frame with U
        RL file:///.../jquery-iframe-auto-height/iframe_2.html
        from frame with URL file:///.../jquery-iframe-auto-height/index.html.
        Domains, protocols and ports must match.
    
        should be fine when code is served from a web server
        view with firefox locally
        -->
      </body>
    </html>
    ```
