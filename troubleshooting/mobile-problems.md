---
description: Symptoms that only appear on phones and tablets.
---

# Mobile and Responsive Problems

Things that look fine on a computer and wrong on a phone. If you're looking for how to *set* a value per device, that's a different article:

{% content-ref url="../other/responsive-settings.md" %}
[responsive-settings.md](../other/responsive-settings.md)
{% endcontent-ref %}

***

### My site looks broken on mobile but fine on desktop

**Check first, in this order:**

1. **Clear all caches.** Mobile is often served a separately cached version of the page, so it can be stale when desktop isn't.
2. **Switch off CSS and JavaScript optimization** temporarily — minify, combine, delay JavaScript. **Combining files is the single most common cause of mobile-only breakage.**
3. **Test on a real device**, not just a narrowed browser window. Some issues only appear with real touch input.

If turning optimization off fixes it, re-enable the settings one at a time until the problem returns.

***

### Content is hidden behind the header

Almost always a transparent header without enough spacing on small screens.

**Customize -> Header -> Transparent Header -> Spacing** — click the **mobile** device icon and increase the value.

This setting is per device, so your desktop value doesn't apply to phones. That's exactly why the problem shows up on mobile only.

***

### The page scrolls sideways

Something on the page is wider than the screen — usually a fixed width or a negative margin set in a page builder.

**To find it:** narrow your browser window to phone width and look for the element extending past the right edge.

**To fix it:** in your page builder, set that element's width as a percentage rather than a pixel value, or give it its own mobile width. Check any custom CSS for fixed pixel widths that should be `max-width` instead.

***

### Hover effects don't work on touch screens

This is expected — phones have no hover. Kalium's portfolio and product hover effects show on tap instead, which means one tap to reveal and a second to follow the link.

**If you'd rather the first tap follow the link**, either choose a hover effect that doesn't overlay content, or turn the hover overlay off for mobile in the relevant **Featured Image** settings.

***

### Parallax looks wrong or feels heavy

Parallax scrolling is expensive on phones and often misaligns.

**The fix:** turn parallax off in the row's settings, or set it per device where the element allows.

Where it doesn't, hide the parallax row on mobile using the row's visibility settings and show a simpler row in its place.

***

### A slider is cut off or the wrong height

Slider sizing belongs to the slider plugin, not to Kalium.

Open the slider's own responsive settings and set the height and layer positions per device.

Also check the padding on the builder row the slider sits in — a fixed-width row will clip a responsive slider no matter what the slider is set to.

***

### Text is too big or too small on phones

Font sizes are per device.

1. **Kalium -> Typography**
2. Open the setting for the element
3. Switch to the **mobile** icon and set the size there

Headings are the usual offender. A 56px display heading that looks striking on a desktop overwhelms a phone screen — 28 to 32px is more typical.

{% content-ref url="../typography/font-sizes.md" %}
[font-sizes.md](../typography/font-sizes.md)
{% endcontent-ref %}

***

### Images look wrong when the grid becomes one column

When a grid reflows to a single column, images of different shapes make the page look untidy.

Set an **Aspect Ratio** in the area's **Featured Image** settings so every image is cropped to the same shape, then regenerate your thumbnails.

{% content-ref url="image-problems.md" %}
[image-problems.md](image-problems.md)
{% endcontent-ref %}

***

### The mobile menu won't open

That has its own article, since it's the most reported mobile issue:

{% content-ref url="header-and-menus.md" %}
[header-and-menus.md](header-and-menus.md)
{% endcontent-ref %}

***

### Testing properly

The Customizer's device preview buttons are useful while you work, but they're an approximation. Before you launch:

* **Open the site on a real phone.** Real devices have different fonts, a browser bar that takes up space, and touch instead of a mouse.
* **Try both orientations.** Landscape catches layout problems portrait hides.
* **Test on both iPhone and Android** if you can. They render some things differently.
