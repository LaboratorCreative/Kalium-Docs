---
description: Blurry, cropped, oversized or slow-loading images.
---

# Image Problems

Nearly every image problem is one of three things: **the wrong size is being loaded**, **the aspect ratio is cropping**, or **thumbnails were never regenerated** after a setting changed.

{% hint style="warning" %}
**Changing an image setting does not resize images you've already uploaded.** After changing an Image Size or Aspect Ratio, you must **regenerate your thumbnails**, otherwise nothing visibly changes and it looks like the setting did nothing.

A plugin such as Regenerate Thumbnails does this, and most hosts offer it too.
{% endhint %}

***

### Images are blurry

The area is displaying an image larger than the size it actually loads.

**Each area has its own Image Size setting**\
Blog, portfolio, search results, product navigation, the lightbox. Find the one for the area you're looking at.

**The fix:**

1. Raise **Image Size** for that area, or set a **Custom Image Size**
2. **Regenerate your thumbnails**
3. If the original upload is small, no setting will help, replace the image with a larger one

Retina screens make this obvious where a standard screen doesn't, so test on the device that showed the problem.

***

### Images are cropped oddly, stretched, or the wrong shape

That's **Aspect Ratio**, not Image Size. It's a separate setting on the same screens, and **it's per device**.

**Set Aspect Ratio to *Original*** to stop cropping entirely and let each image keep its own shape.

**Or choose a ratio** and let the theme crop everything consistently, which usually looks tidier in a grid.

Check tablet and mobile separately. A ratio that works on desktop can crop badly on a phone.

{% content-ref url="../other/responsive-settings.md" %}
[responsive-settings.md](../other/responsive-settings.md)
{% endcontent-ref %}

***

### Everything became oversized after an update

If font sizes and images both scaled up together, the images aren't the cause, the layout is.

Check **Customize -> Styling -> Layout -> Block Spacing** and the container width against the values you had before.

If you never changed them, an upgrade from Kalium 3 re-based some spacing values.

{% content-ref url="after-an-update.md" %}
[after-an-update.md](after-an-update.md)
{% endcontent-ref %}

***

### Images fill the whole column instead of their set size

Check your custom CSS for width rules on image containers. This is usually a custom rule interacting with the theme's own image sizing.

If you have no custom CSS doing that, update the theme, sizing fixes have shipped in several releases.

***

### The lightbox is slow to open

It's loading full-size originals. A photo straight from a phone can be several megabytes.

**Customize -> General -> Lightbox Settings -> Main Image**\
Change it from *Full Size* to *Large*.

The difference is dramatic and the quality loss is usually invisible on screen.

{% content-ref url="../other/lightbox.md" %}
[lightbox.md](../other/lightbox.md)
{% endcontent-ref %}

***

### Image quality looks worse than the file I uploaded

WordPress recompresses uploads by default. Kalium lets you control how much.

**Customize -> Performance -> JPEG Image Quality**\
Raise it, then regenerate your thumbnails.

This affects new uploads and regenerated sizes only, which is why the regeneration step matters.

***

### Images don't load at all

1. **Open a broken image in a new tab** and look at its address. If it contains an old or staging domain, the problem is the address. Run a search-and-replace across the database for the old domain.
2. **Clear all caches**, including your CDN.
3. **Check the file exists** in **Media** in your admin.

{% content-ref url="after-an-update.md" %}
[after-an-update.md](after-an-update.md)
{% endcontent-ref %}

***

### Images are missing after importing a starter site

Media is imported last and is the slowest step, so a stall leaves you with content and no pictures.

{% content-ref url="starter-site-imports.md" %}
[starter-site-imports.md](starter-site-imports.md)
{% endcontent-ref %}

***

### Getting images right from the start

* **Upload at a reasonable size.** 2000px on the longest edge is plenty for most sites. Straight-from-camera files are far larger than any screen needs.
* **Use consistent shapes** within a grid, set an aspect ratio and let the theme crop.
* **Regenerate thumbnails** after any image setting change. It's the step everyone forgets.
* **Compress before uploading**, or use an optimization plugin. It's the single biggest thing you can do for page speed.
