---
title: "Images"
description: "Add a small or large image with a Doks shortcode (add extra classes), or use markdown (portability). Images are lazyloaded, blurred up, and responsive."
lead: "Add a small or large image with a Doks shortcode (add extra classes), or use markdown (portability). Images are lazyloaded, blurred up, and responsive."
date: 2020-11-23T11:53:06+01:00
lastmod: 2020-11-23T11:53:06+01:00
draft: false
images: []
menu:
  docs:
    parent: "recipes"
weight: 160
toc: true
---

Place your images in a page bundle, like so:

```bash
..
├── blog/
│   ├── say-hello-to-doks/
│   │   ├── index.md
│   │   └── say-hello-to-doks.png
│   └── _index.md
└── _index.md
```

See also the Hugo docs: [Page Bundles](https://gohugo.io/content-management/page-bundles/)

## Markdown

### Add an image

An `<img>` element is used for small images, a `<figure>` element for large images. Set `smallLimit` in `./config/_default/params.toml`, e.g. `smallLimit = "360"`.

#### Example

```md
![Image](day-and-night-escher.jpg "Day and Night, 1938 — M.C. Escher")
```

Will be processed into:

![Image](day-and-night-escher.jpg "Day and Night, 1938 — M.C. Escher")

See also the Markdown Guide: [Images](https://www.markdownguide.org/basic-syntax/#images-1)

## Shortcodes

### Add a small image

Using `img`, `src`, and `data-src`.

{{< alert icon="💡" text="Valid image formats are: webp, jpg, png, tiff, bmp, and gif." />}}

Add a small image in your page bundle to your page using shortcode `img-simple`.

#### Example

```bash
{{</* img-simple src="square.png" alt="Square" class="border-0 rounded-circle" */>}}
```

Will be processed into:

{{< img-simple src="square.png" alt="Square" class="border-0 rounded-circle" >}}

### Add a large image

Using `figure` and `figcaption` with `img`, `src`, and `data-srcset`. With `noscript` fallback.

{{< alert icon="💡" text="Valid image formats are: webp, jpg, png, tiff, and bmp." />}}

Add a large image in your page bundle to your page using shortcode `img`.

#### Example

```bash
{{</* img src="rectangle.png" alt="Rectangle" caption="<em>Rectangle</em>" class="border-0" */>}}
```

Will be processed into:

{{< img src="rectangle.png" alt="Rectangle" caption="<em>Rectangle</em>" class="border-0" >}}
