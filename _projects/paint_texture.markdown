---
layout: page
title: Dynamic Paint Textures
description: Simulating paint textures on mobile screens
img: /assets/img/gelProto.jpg
importance: 2
---

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        <img class="img-fluid rounded z-depth-1" src="{{ '/assets/img/gelProto.jpg' | relative_url }}" alt="" title="example image"/>
    </div>
</div>
<div class="caption">
    
</div>

## Abstract

Digital painting is an increasingly popular medium of expression for many artists, yet when compared to its traditional equivalents of physical brushes and viscus paint it lacks a dimension of tangibility. We conducted observations and in- terviews with physical and digital artists, which gave us a strong understanding of the types of interactions used to create both physical and digital art, and the important role tangibility plays within these experiences. From this, we developed a unique liquid-like tangible display for mobile, digital colour mixing. Using a chemical hydrogel that changes its viscosity depending on temperature, we are able to simulate the tangible feeling of mixing paint with a finger. This paper documents the information gathered from working with artists, how this process informed the development of a mobile painting attach- ment, and an exploration of its capabilities. We then document the feedback gathered from the artists, after returning with the prototype. We learnt it provided them with sensations of oil and acrylic paint mixing, while also successful mimicked how paints are laid out on a paint palette. {% cite steerLiquidTangibleDisplay2018 %}

## Prototype

The final interaction of the prototype allowed the user to hold the device in a single hand with their fingers on the back to reach the gel, while their thumb on the front screen is able to select the desired starting colour. It also moves us towards envisioning the gel palette in the form of a mobile accessory that can be added to any standard mobile device. The user begins their interaction by picking the colour on the phone app. This imitates how an artist would pick out their starting paints to place on the palette. Once the colour is set, the gel on the back of the phone can now be manipulated, as touch sensing and temperature control in that area is now active.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        <img class="img-fluid rounded z-depth-1" src="{{ '/assets/img/temp-change.png' | relative_url }}" alt="" title="example image"/>
    </div>
</div>
<div class="caption">
    Hydrogel states as temperature is changed, Left: The gel is at its hardest, feeling like an oil-based paint. Centre: The gel is softer and thinned out, feeling more like an acrylic-based paint. Right: The gel is now at its softest after being fully thinned out, and feels more like a water-based paint.
</div>


When the user touches the back of the mirrored location of the paint on the screen, the touch is registered as an interaction. From this point, the user can push and rub the gel. This will cause the gel to be actuated towards a softer state. The user will see the colour on the phone screen decrease in saturation. This interaction process simulates the paints to thin in order to alter their shade. Once the user has mixed their desired saturation, they can select it with their finger or stylus on the phone screen. They then use the colour on the canvas application. Our technical implementation of the prototype is layered to provide the temperature actuation. The hydrogel sits under a layer of polyurethane on top of the resistive touchscreen. This screen then sits on a 4x3 array of Peltier modules, each with a 15x15mm activation layer. Each Peltier module can cool or heat the gel. This is controlled by an IC chip, so by using an Arduino, we can switch the H-Bridge within the chip for each Peltier to either cool the gel making it appear soft or heat it to appear stiff. In order for the Peltier to efficiently cool the hydrogel, we add a heat sink underneath the grid. This disperses the heat from the hot side of the Peltier and cools the active side. This activation layer is then attached to the back of the iPhone. 

As all interactions from the back of the device needed to translate to how the paint is displayed on the front screen, we developed a paint mixing app. This iPhone app connects via Bluetooth to the prototype attachment. This allows the app to translate the coordinates of the interactions with the gel transmitted and display paint on the front screen. The app starts by displaying a set of primary colours (red, yellow and blue). From here, users can then drag these colours to other areas of the screen and mix them with other colours, all using the back of the device. Where the colours are dragged, these areas will also actuate to soft when the Peltier cools down the hydrogel where the paint runs from point to point. The application pairs with an iPad app that presents a canvas. Users pick the colour on the iPhone app with a stylus or finger, which they use to paint on the canvas. Our iPad app offers basic tools such as nib size adjustment and an erasure. 

## Project Outcomes

<div class="publications">
  {% bibliography --cited %}
</div>

<strong>Talk from MobileHCI 2018</strong>
<div class="row">
    <div class="col-sm mt-3 mt-md-0">    
        <iframe width="560" height="315" src="https://www.youtube.com/embed/TZU3UKNzi58" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>
    </div>
</div>





