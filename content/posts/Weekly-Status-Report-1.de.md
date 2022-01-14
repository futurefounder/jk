---
title: "📡 Wöchentlicher Status Report #1"
date: 2021-05-15T11:14:27+02:00
draft: false
showToc: false
comments: false
ShowBreadCrumbs: false
---

Was letzte Woche passiert ist - 10.05 - 14.05.2021

**Das Gute**

RemoteNActive

- Ich habe die deutsche Website live und zum laufen bekommen
- Ich habe verschiedene Möglichkeiten zur Optimierung der Website-Geschwindigkeit erarbeitet
    - Optimierung der Bildgröße
    - Verzögerung der Iframe-Auslieferung über jQuery / Javascript

Code zum Verzögern des Iframes (einschließlich OnClick Confetti, weil ... Confetti;)

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

- Website-Geschwindigkeit optimiert: Desktop sieht sehr gut aus.

![https://i.ibb.co/RPvXZNS/remotenactive-desktop.png](https://i.ibb.co/RPvXZNS/remotenactive-desktop.png)

- Soft-Launch per Nachrichten an Freunde und ehemalige Arbeitskollegen

**Das Schlechte**

RemoteNActive

- Englische Website noch nicht live
- Die Geschwindigkeit der mobilen Site ist noch nicht so optimal.

![https://i.ibb.co/PFWjNS0/remotenactive-mobile.png](https://i.ibb.co/PFWjNS0/remotenactive-mobile.png)

- Der Grund scheint zu sein, dass ich Tailwind per CDN verwende, das viel CSS enthält, das ich nicht benötige, und dies verlangsamt die mobile Version der Website. Fix ist höchstwahrscheinlich Tailwind lokal zu installieren und nur das CSS zu kompilieren, das ich benötige.
- Ich habe eine Absage  von einem Interessenten bekommen 🤷🏽‍♂️
- Ich muss meine monatlichen und wöchentlichen Ziele klarer festlegen

**Das Hässliche**

- Die Website ist eher mit externem Javascript aufgebläht
- Keine Case-Study bisher

**Was kommt als Nächstes?**

- Hauptpriorität ist es, meine ersten 4 Fallstudienkunden zu finden
    - Entweder durch meine persönlichen Kontakte
    - Oder mit dem bezahlten Marketing beginnen