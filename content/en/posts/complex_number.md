---
title: "Complex Numbers & Polar Coordinates"
date: 2024-01-24T13:47:22-06:00
lastmod: 2024-02-03T13:47:22-06:00
author: "Weifan Zhou"
slug:
draft: false
toc: false
---
This is a complex number: $$z = x + iy$$
A complex number, as a combination of a real number (<code>$x$</code>) and an imagenary number (<code>$iy$</code>, or <code>$yi$</code>, it doesn't matter) can be sketched with 2-dimentional axis. Note that <code>$y$</code> is a real number, and <code>$i$</code> is an imagenary number (<code>$i = \sqrt{-1}$</code>).

This is an example from [mathbits](https://mathbitsnotebook.com/Algebra2/ComplexNumbers/CPGraphs.html):
<figure itemprop=associatedMedia itemscope itemtype=http://schema.org/ImageObject>
<a href=/media/complex_num1.jpg itemprop=contentUrl>
<img itemprop=thumbnail src=/media/complex_num1.jpg width="300" style="display: block; margin: 0 auto" alt="sketch complex number">
</a>
</figure>

The real axis represents the real number <code>$x$</code>, with each unit representing 1. The imagenary axis represents the imagenary part <code>$iy$</code>, each unit representing <code>$i$</code>, and <code>$y$</code> represents the number of units.

Also, to represent an complex number with number pairs, we can use the format of <code>$(x, y)$</code>. For example, <code>$i=2+3i$</code> can be noted down as <code>$(2,3)$</code>.

If you have learned Calc 2, you may have heard about polar coordinates. We can also use polar system to sketch complex numbers. 

For example, <code>$z=x+iy$</code> can be represented as:
 $$z= r(\cos{\theta}+i\sin{\theta})$$
Here is an image copied from [Online Math Learning Website](https://www.onlinemathlearning.com/complex-plane-hsn-cn4.html):
<figure itemprop=associatedMedia itemscope itemtype=http://schema.org/ImageObject>
<a href=/media/complex_num2.jpg itemprop=contentUrl>
<img itemprop=thumbnail src=/media/complex_num2.jpg width="400" style="display: block; margin: 0 auto" alt="sketch complex number">
</a>
</figure>

To use pairs, we can note down in <code>$(r, \theta)$</code> form. For example, <code>$z=1+i$</code> can be represented as <code>$(\sqrt{2}, \frac{\pi}{4})$</code> (45 degree angle), or to be more cautious let's write down <code>$(\sqrt{2},\frac{\pi}{4}+2k\pi)$</code>, if you rotate extra 360 degrees, 720 degrees, etc. You are back to where 45 degree line locates.

If you have learned Calc 2, you may also have heard of Taylor Series. You can use Taylor Series to get a wierd form:
$$\cos{\theta}+i\sin{\theta}=e^{i\theta}$$

Here is a proof from YouTube: <iframe width="560" height="315" src="https://www.youtube.com/embed/GqvDUcU8F3I?si=VGYh7lccROpKH5nW" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

Then, the complex number <code>$z=x+iy$</code> can be represented as:
 $$z=r(\cos{\theta}+i\sin{\theta})=re^{i\theta}$$

When you have the <code>$e$</code> form of the complex number, if you would like to calculate the root or power of it, it's becoming simpler.

Hmm, why do I care about this?
Well, if someone ask you to calculate the root of complex numbers, the power of complex numbers, the mod of complex number, all the process gets easier.

For example, how to calculate <code>$\left|\left(\frac{1+i}{1-i}\right)^5\right|$</code>? I mean the mode, or the length of <code>$\left(\frac{1+i}{1-i}\right)^5$</code>.
You can calculate the power first, or you can calculate the faction, but I am too lazy to do that. What about using the magical <code>$re^{i\theta}$</code>?

$$ \left|\left(\frac{1+i}{1-i}\right)^5\right|
= \left|\left(\frac{\sqrt{2}e^{i(\frac{\pi}{4})}}{\sqrt{2}e^{i(-\frac{\pi}{4})}}\right)^5\right|
= \left|\left(e^{i\frac{\pi}{2}}\right)^5\right|
= \left|e^{i\frac{5\pi}{2}}\right|
= 1$$

Apologize: I am too lazy to type out the case of <code>$2k\pi$</code> and draw the curve.