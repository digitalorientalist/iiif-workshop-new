---
menuTitle: "Detailed Example"
date: 2018-04-15T13:59:05-04:00
weight: 10
---

# Detailed Image API Parameters Example

Here's a visual tour of how you can extract a region and manipulate the image further.

We'll start with the full size version of this image and crop out just the building. You can see where the architect was testing out colors, so it'd be nice to crop those out.

The resource we'll use is [Perspective from the West - Front by Henry L. Kamphoefner](https://d.lib.ncsu.edu/collections/catalog/mc00198-008-ff0051-000-001_0001).

![](https://iiif.lib.ncsu.edu/iiif/mc00198-008-ff0051-000-001_0001/full/800,/0/default.jpg)

This is the URL we will end up with:

<!-- #todo:110 some sort of fraction formatting going on here? -->

`https://iiif.lib.ncsu.edu/iiif/mc00198-008-ff0051-000-001_0001/2016,2280,1884,952/500,/0/default.jpg`

Let's walk through it.

## Image Server Base URL

Highlighted is the portion of the URL that would be the same for all of the images delivered from the same image server.

> <a href="https://iiif.lib.ncsu.edu/iiif/mc00198-008-ff0051-000-001_0001/2016,2280,1884,952/500,/0/default.jpg" target=_blank><strong><span>https://</span>iiif.lib.ncsu.edu/iiif/</strong>mc00198-008-ff0051-000-001_0001/2016,2280,1884,952/500,/0/default.jpg</a>

## Identifier

The identifier is: `mc00198-008-ff0051-000-001_0001`

> <a href="https://iiif.lib.ncsu.edu/iiif/mc00198-008-ff0051-000-001_0001/2016,2280,1884,952/500,/0/default.jpg" target=_blank><span>https://</span>iiif.lib.ncsu.edu/iiif/<strong>mc00198-008-ff0051-000-001_0001</strong>/2016,2280,1884,952/500,/0/default.jpg</a>

## Region

> <a href="https://iiif.lib.ncsu.edu/iiif/mc00198-008-ff0051-000-001_0001/2016,2280,1884,952/500,/0/default.jpg" target=_blank><span>https://</span>iiif.lib.ncsu.edu/iiif/mc00198-008-ff0051-000-001_0001/<strong>2016,2280,1884,952</strong>/500,/0/default.jpg</a>

Our single `xywh` parameter value is `2016,2280,1884,952`. We can break out the individual parameters like this:

| parameter | value |
|:----------|:------|
| x         | 2016  |
| y         | 2280  |
| w         | 1884  |
| h         | 952   |

### Region: x

To get the `x` position we count over 2016 pixels.

![](/images/kamp-small-x.jpg)

### Region: y

We then go down from the top by 2280 pixels to get the `y` position.

![](/images/kamp-small-xy.jpg)

### Region: xy Point

What we're really doing is selecting the `xy` point on the image.

![](/images/kamp-small-xy-point.jpg)

### Region: w

From that xy point we measure out the width in pixels.

![](/images/kamp-small-w.jpg)

### Region: h

Finally from the xy point we measure out the height in pixels.

![](/images/kamp-small-h.jpg)

### Selected Region

Here's the region we've selected from the full image based on our `xywh` parameters.

![](/images/kamp-small-xywh-highlighted.jpg)

### Full Size Image of Selected Region

<div class="allow-overflow">
  <img src="https://iiif.lib.ncsu.edu/iiif/mc00198-008-ff0051-000-001_0001/2016,2280,1884,952/full/0/default.jpg">
</div>

## Size

That's still quite a large image so we can scale the image down. In this case the image is scaled down to 500 pixels and the height is scaled proportionally. We'll see other examples of possible size values in the next section.

> <a href="https://iiif.lib.ncsu.edu/iiif/mc00198-008-ff0051-000-001_0001/2016,2280,1884,952/500,/0/default.jpg" target=_blank><span>https://</span>iiif.lib.ncsu.edu/iiif/mc00198-008-ff0051-000-001_0001/2016,2280,1884,952/<strong>500,</strong>/0/default.jpg</a>

![](https://iiif.lib.ncsu.edu/iiif/mc00198-008-ff0051-000-001_0001/2016,2280,1884,952/500,/0/default.jpg)

## Rotation

Let's say we wanted to rotate the image 180 degrees. Our URL would look like this:

> <a href="https://iiif.lib.ncsu.edu/iiif/mc00198-008-ff0051-000-001_0001/2016,2280,1884,952/500,/180/default.jpg" target=_blank><span>https://</span>iiif.lib.ncsu.edu/iiif/mc00198-008-ff0051-000-001_0001/2016,2280,1884,952/500,/<strong>180</strong>/default.jpg</a>

![](https://iiif.lib.ncsu.edu/iiif/mc00198-008-ff0051-000-001_0001/2016,2280,1884,952/500,/180/default.jpg)

## Quality

We requested the default quality through. We could also ask for a gray version:

> <a href="https://iiif.lib.ncsu.edu/iiif/mc00198-008-ff0051-000-001_0001/2016,2280,1884,952/500,/0/gray.jpg" target=_blank><span>https://</span>iiif.lib.ncsu.edu/iiif/mc00198-008-ff0051-000-001_0001/2016,2280,1884,952/500,/0/<strong>gray</strong>.jpg</a>

![](https://iiif.lib.ncsu.edu/iiif/mc00198-008-ff0051-000-001_0001/2016,2280,1884,952/500,/0/gray.jpg)

## Format

We request a JPEG image:

> <a href="https://iiif.lib.ncsu.edu/iiif/mc00198-008-ff0051-000-001_0001/2016,2280,1884,952/500,/180/default.jpg" target=_blank><span>https://</span>iiif.lib.ncsu.edu/iiif/mc00198-008-ff0051-000-001_0001/2016,2280,1884,952/500,/180/default.<strong>jpg</strong></a>

<!-- #todo:0 remove awful spans around https:// trick to prevent creation of links for link checker -->
