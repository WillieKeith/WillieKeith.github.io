---
title: "From ArcMap to QGIS -- Basics (1)"
date: 2024-06-22T22:54:25-04:00
author: "Weifan Zhou"
slug:
draft: false
toc: false
---
This year, ArcMap has retired. It's time to transform to a new mapping software. Many universities start using ArcGIS Pro, a paid software made from the same company as ArcMap.

Oh, you don't have a liscense? Or you use MacOS or Linux. Here's another option: you can use QGIS, which is free. Mapping softwares are similar.

I will NOT provide steps in detail because that's gonna be quite long. But I recommend you type in those questions on google, YouTube or ChatGPT, which will give you solid answers.

#### Rough Ideas

1. How to add a layer?
- You can go to Layer -- Data Source Manager -- Vector. To add your file, click the three dot... Find your shapefile and add it.
<figure itemprop=associatedMedia itemscope itemtype=http://schema.org/ImageObject>
<a href=/media/qgis/image-1.jpg itemprop=contentUrl>
<img itemprop=thumbnail src=/media/qgis/image-1.jpg width="300" style="display: block; margin: 0 auto" alt="add a layer">
</a>
</figure>

2. Select by attribute?
- In QGIS it's not called "select by attribute". Instead, it's called "select features by value" or "select features by expression". Watch this video:
<iframe width="560" height="315" src="https://www.youtube.com/embed/jPXSMBgA8Rg?si=2E7_hP6Y1xWw8GCi" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

3. Select by location?
- This one:
- <figure itemprop=associatedMedia itemscope itemtype=http://schema.org/ImageObject>
<a href=/media/qgis/image-2.jpg itemprop=contentUrl>
<img itemprop=thumbnail src=/media/qgis/image-2.jpg width="30" style="display: block; margin: 0 auto" alt="select by location icon">
</a>
</figure>


4. Change the coordinate system?
- Right click on your layer -- layer CRS.

5. Where's print layout? Legend? Arrow? Blablabla?
- Look here: 
- <figure itemprop=associatedMedia itemscope itemtype=http://schema.org/ImageObject>
<a href=/media/qgis/image-3.jpg itemprop=contentUrl>
<img itemprop=thumbnail src=/media/qgis/image-3.jpg width="300" style="display: block; margin: 0 auto" alt="layer CRS">
</a>
</figure>
- If you need to see the print layout that you've already created, go to layout manager instead.
- To be more in detail, I think this article will answer your question: <a href = "https://medium.com/introduction-to-critical-spatial-media-beyond-the/qgis-print-layout-end-exporting-8a32f5294edb">QGIS Print Layout and Exporting</a>. 

6. How to insert a secondary map in layout view? How to add a new dataframe.
- Well... Currently, I don't know how to add a new dataframe. But one way is to create another map file, export the second map into an image, and insert that image to the first map.

7. How to add XY data?
- Make sure you data is csv. If you wish to import xls directly, you can also add a plugin (I forgot which one. Please search it on google).
- Check this video.<iframe width="560" height="315" src="https://www.youtube.com/embed/Qo8PM8Qsqwk?si=iG6WohchXl9HFLlp" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
