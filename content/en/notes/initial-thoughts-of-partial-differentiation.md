---
title: "Initial Thoughts of Partial Differentiation"
date: 2024-02-29T16:15:04-06:00
author: "Weifan Zhou"
slug:
draft: false
toc: false
---
As a person who've only completed Calc 1 & 2, I just started learning some partial differentiation. The symbol of partial differentiaion is a bit confused to me at first, but there's an easier way of thinking about differentiaion in 3-dimentional cases: cutting cakes.

When you plan to cut a cake, you can either cut it in two ways: you can cut it from left to right, or from front to back.

<figure itemprop=associatedMedia itemscope itemtype=http://schema.org/ImageObject>
<a href=/media/Cake.jpg itemprop=contentUrl>
<img itemprop=thumbnail src=/media/Cake.jpg width="300" style="display: block; margin: 0 auto" alt="Imagine a complete Cake whose length and with is x and y, and whose height at each point of the surface is f(x,y)">
</a>
</figure>

Imagine a complete Cake whose length and with is x and y, and whose height at each point of the surface is f(x,y). Then you cut it from left to right, parallel to the x axis.

<figure itemprop=associatedMedia itemscope itemtype=http://schema.org/ImageObject>
<a href=/media/Cut_cake.jpg itemprop=contentUrl>
<img itemprop=thumbnail src=/media/Cut_cake.jpg width="300" style="display: block; margin: 0 auto" alt="Then you cut it from left to right, parallel to the x axis">
</a> You got a beautiful slice.
</figure>

Move your eye to the right side of the whole big cake, and look at the thin slice. Then chop the little slice along the x axis. Now each little smaller slice looks like a chip (french fries).

<figure itemprop=associatedMedia itemscope itemtype=http://schema.org/ImageObject>
<a href=/media/sight.jpg itemprop=contentUrl>
<img itemprop=thumbnail src=/media/sight.jpg width="300" style="display: block; margin: 0 auto" alt="Now each little smaller slice looks like a chip (french fries)">
</a> Look at the height of the little cake chip (fries)!
</figure>

Hey, those chips (fries) are thin. Imagine they are too thin to let you notify the width. Only look at the height of each chip (fries)! They are changing as the height of the cream is changing, moving up and down.

Think about this cake slice, that your y is static. The difference for each "cake chip (fries)" is that they have different x but the same y. 

<figure itemprop=associatedMedia itemscope itemtype=http://schema.org/ImageObject>
<a href=/media/chip-into-function.jpg itemprop=contentUrl>
<img itemprop=thumbnail src=/media/chip-into-function.jpg width="300" style="display: block; margin: 0 auto" alt="Now each little smaller slice looks like a chip (french fries)">
</a> Let's abstract the chip (fries) height into a function.
</figure>

Look at the slope of this chip (fries) height function! We can say the slope of this function is df/dx when y=0.

However, if you cut a different cake slice from left to right (cut parallel to x, but choose a different y), for example, in the middle which contains the cherry, that slice will give you a different height. It's no longer like a perfect wave, but you will see the strange cherry tip that makes the middle of the function suddenly goes higher. 

Similarly, you can cut from front to back. In this case, x is static for each slice, while y is changing for each chip. How should you represent the slope of this function?

(To be continued...)