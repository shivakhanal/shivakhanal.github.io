---
title: "Forest inventory in Mountains"
header:
  overlay_image: assets/image/mountain.png
  caption: #"Photo credit: [**Unsplash**](https://unsplash.com)"
  actions:
    - label: "Call to action 1"
      url: "https://github.com/shivakhanal"
    - label: "Call to action 2"
      url: "https://github.com/shivakhanal"
categories:
  - Layout
  - Uncategorized
tags:
  - edge case
  - image
  - layout
last_modified_at: 2016-05-02T11:39:01-04:00
---

This post should display some examples of forest inventory  activities.  

Non-square images can provide some unique styling issues.

This post tests overlay header images. 'assets/image/mountain.png'

## Overlay filter

You can use it by specifying the opacity (between 0 and 1) of a black overlay like so:

![transparent black overlay]({{ 'assets/image/DSC01270.jpg' | relative_url }})

```yaml
excerpt: "This post should [...]"
header:
  overlay_image: /assets/image/unsplash-image-1.jpg
  overlay_filter: 0.5 # same as adding an opacity of 0.5 to a black background
  caption: "Photo credit: [**Unsplash**](https://unsplash.com)"
  actions:
    - label: "More Info"
      url: "https://unsplash.com"
```

Or if you want to do more fancy things, go full rgba:

![transparent red overlay]({{ 'assets/image/mountain.png' | relative_url }})

```yaml
excerpt: "This post should [...]"
header:
  overlay_image: /assets/image/unsplash-image-1.jpg
  overlay_filter: rgba(255, 0, 0, 0.5)
  caption: "Photo credit: [**Unsplash**](https://unsplash.com)"
  actions:
    - label: "More Info"
      url: "https://unsplash.com"
```