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

<div class = "reminder">I will NOT provide steps in detail because that's gonna be quite long. But I recommend you type in those questions on google, YouTube or ChatGPT, which will give you solid answers.</div>

## Rough Ideas

### 1. How to Add a Layer?
- Navigate to **Layer** > **Data Source Manager** > **Vector**. To add your file, click the three dots (...) to find your shapefile and add it.
<figure itemprop="associatedMedia" itemscope itemtype="http://schema.org/ImageObject">
  <a href="/media/qgis/image-1.jpg" itemprop="contentUrl">
    <img itemprop="thumbnail" src="/media/qgis/image-1.jpg" width="600" style="display: block; margin: 0 auto" alt="add a layer">
  </a>
</figure>

### 2. Select by Attribute?
- In QGIS, it's called "Select Features by Value" or "Select Features by Expression". Watch this video:
<iframe width="560" height="315" src="https://www.youtube.com/embed/jPXSMBgA8Rg?si=2E7_hP6Y1xWw8GCi" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

### 3. Select by Location?
- Use the following icon:
<figure itemprop="associatedMedia" itemscope itemtype="http://schema.org/ImageObject">
  <a href="/media/qgis/image-2.jpg" itemprop="contentUrl">
    <img itemprop="thumbnail" src="/media/qgis/image-2.jpg" width="30" style="display: block; margin: 0 auto" alt="select by location icon">
  </a>
</figure>

### 4. Change the Coordinate System?
- Right-click on your layer and select **Layer CRS**.

### 5. Where's Print Layout? Legend? Arrow? Etc.?
<figure itemprop="associatedMedia" itemscope itemtype="http://schema.org/ImageObject">
  <a href="/media/qgis/image-3.jpg" itemprop="contentUrl">
    <img itemprop="thumbnail" src="/media/qgis/image-3.jpg" width="300" style="display: block; margin: 0 auto" alt="layer CRS">
  </a>
</figure>

- To view the print layout you've created, go to **Layout Manager**.
- For more details, this article will help: [QGIS Print Layout and Exporting](https://medium.com/introduction-to-critical-spatial-media-beyond-the/qgis-print-layout-end-exporting-8a32f5294edb).

### 6. How to Insert a Secondary Map in Layout View? How to Add a New Dataframe?
- Currently, I'm not sure how to add a new dataframe. One workaround is to create another map file, export the second map as an image, and insert that image into the first map.

### 7. How to Add XY Data?
- Ensure your data is in CSV format. If you need to import XLS directly, you can add a plugin (search for the appropriate plugin on Google).
- Check out this video for more information:
<iframe width="560" height="315" src="https://www.youtube.com/embed/Qo8PM8Qsqwk?si=iG6WohchXl9HFLlp" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>