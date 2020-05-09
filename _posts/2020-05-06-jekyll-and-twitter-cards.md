---
layout: post
title: ✏️ How to implement Twitter Cards with Jekyll
subtitle: That took some research
illustration: https://avatars1.githubusercontent.com/u/3083652?s=400&v=4
categories: [blog]
tags: [tuto, jekyll, twitter]
comments: true
---



### Adding Twitter cards was not as easy as I first though. Here is how I did it.



So now that I'm tinkering a little bit with this website, I wanted to have nice Twitter Cards to share when publishing a new post or article. 

My googlefu gave me a lot of answers but I kept on having on error when validating the card on Twitter's side. Here's how you do it with a static website build with Jekyll.  



#### First the metatags

You will have to put this in your header. You can have it in an include file. I'm not confident enough with that so I put everything in my default.html in  <head>.

```html 
<!-- Twitter cards -->
<meta name="twitter:site" content="@USERNAME">
<meta name="twitter:text:title" content="page.title">
<meta name="twitter:creator" content="@USERNAME">
<meta name="twitter:title" content="page.title">

{% if page.subtitle %}
<meta name="twitter:description" content="page.subtitle">
{% else %}
<meta name="twitter:description" content="site.description">
{% endif %}

{% if post.illustration %}
<meta name="twitter:card"  content="summary_large_image">
<meta name="twitter:image" content="page.illustration">
{% else %}
<meta name="twitter:card"  content="summary">
<meta name="twitter:image" content="site.avatar">
{% endif %}
<!-- end of Twitter cards -->
```

**!!Remark: the liquid tag here (e.g. page.title) must be inside double curly brackets otherwise it would not process the request.**

I couldn't put them that way in this markdown code snippets are they were processed in the HTML conversion. I'm still looking for a way to do that.

Once it's done, you will have to validate your card by parsing your URL it at this address:  [https://cards-dev.twitter.com/validator](https://cards-dev.twitter.com/validator). Don't use your base URL has it would not pass due to the fact that some metatags will be missing (page.title for example).

The bit that got me confused was that I always had this error while previewing the card: 

>ERROR: Required meta tag missing (twitter:text:title)

And there is little to no information on the internet about this error when it comes to Jekyll, while a lot of people had it solved with Wordpress. So it was just a matter of adding this metatag and parse him the *page.title* tag.

Now my only problem is that *page.illustration* are not taken into account when Twitter creates the card. That's something I'm still looking at.