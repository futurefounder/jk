---
title: "📡 Weekly Status Report #1"
date: 2021-05-15T11:14:27+02:00
draft: false
showToc: false
comments: false
ShowBreadCrumbs: false
---

What happened last week - 10.05 - 14.05.2021

**The good**

RemoteNActive

- I got the German Website live and running
- Discovered various ways to optimize site speed via
    - Image size optimization
    - Delaying iframe output via jQuery/Javascript

Code to delay iframe (including OnClick Confetti, because... Confetti ;) 

{{< highlight html >}}
<script type="text/javascript" src="https://ajax.googleapis.com/ajax/libs/jquery/1.6.0/jquery.min.js"></script>

<script type="text/javascript">

$(function(){

$('#buttonframe').click(function(){

if(!$('#iframe').length) {

$('#iframeHolder').html('<iframe src="URL-to-canvas-here"> </iframe>');

}

function randomInRange(min, max) {

return Math.random() * (max - min) + min;

}

confetti({

angle: randomInRange(55, 125),

spread: randomInRange(50, 70),

particleCount: randomInRange(50, 100),

origin: { y: 0.6 }

});

});

});

</script>
{{< /highlight >}}

- Site Speed optimized: Desktop looks very good.

![https://i.ibb.co/RPvXZNS/remotenactive-desktop.png](https://i.ibb.co/RPvXZNS/remotenactive-desktop.png)

- Soft-Launch by messaging friends and ex-work colleagues

**The bad**

RemoteNActive

- English Website not live yet
- Mobile Site speed is not so optimal.

![https://i.ibb.co/PFWjNS0/remotenactive-mobile.png](https://i.ibb.co/PFWjNS0/remotenactive-mobile.png)

- The reason seems to be that I use Tailwind via CDN which has a lot of CSS which I do not need and this slows down the mobile version of the website. Fix is most likely to install Tailwind locally and compile only the CSS I need.

- Got one decline from a prospect 🤷🏽‍♂️
- I have to set my monthly and weekly goals clearer

**The ugly**

- Website is rather bloated with external javascript
- No case study yet

**What's next?**

- Main priority is to find my first 4 case study clients
    - Either through my personal contacts
    - Or starting paid marketing
