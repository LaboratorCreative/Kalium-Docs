---
description: >-
  Kalium works with Elementor, WPBakery and the built-in WordPress editor, and
  adds its own elements to each.
---

# Page Builders

Kalium doesn't tie you to one way of building pages. Three editors are supported, and Kalium adds its own elements to each of them so you can drop a portfolio grid or a blog listing into a page without writing anything.

You can use more than one on the same site, a page built with Elementor sits happily beside one built with the block editor. What you can't do is build the *same* page with two of them.

***

### Which one should you use?

**The WordPress block editor** is built into WordPress. Nothing to install, fast, and perfectly capable for most pages. Start here if you're not sure.

**Elementor** is a full visual editor with drag-and-drop and live preview. The most popular choice, and the one with the largest ecosystem of add-ons. Best if you want fine control over layout without touching code.

**WPBakery** is the long-established builder bundled with Kalium. Most of the Kalium starter sites are built with it, so if you imported one, this is probably what you're already using.

{% hint style="info" %}
**If you imported a starter site**, keep using whichever builder it was built with. Rebuilding a page in a different builder means starting that page again from scratch.
{% endhint %}

***

### What Kalium adds to each

| Element | Block editor | Elementor | WPBakery |
| --- | :---: | :---: | :---: |
| **Portfolio Items** | Yes | Yes | Yes |
| **Blog Posts** | Yes | Yes | Yes |
| **Content Section** | Yes | Yes | Yes |
| 24 more elements | | | Yes |

All three builders get the same three core elements. WPBakery has many more, because Kalium has supported it the longest.

{% content-ref url="block-editor.md" %}
[block-editor.md](block-editor.md)
{% endcontent-ref %}

{% content-ref url="elementor.md" %}
[elementor.md](elementor.md)
{% endcontent-ref %}

{% content-ref url="wpbakery.md" %}
[wpbakery.md](wpbakery.md)
{% endcontent-ref %}

***

### The three shared elements

**Portfolio Items**\
A grid of projects, with the same layout and filtering options as a portfolio page. Only appears when the portfolio module is enabled under **Kalium -> Settings -> Portfolio**.

**Blog Posts**\
A listing of posts, with control over how many, which categories, and how they're laid out.

**Content Section**\
Drops a Template Part of type *Section* into the page. Handy when one page needs a section and no display condition would express that neatly. Only appears while Template Parts is enabled.

***

### Installing a builder

Elementor and WPBakery are both offered through **Kalium -> Plugins**, along with everything else the theme bundles. Install from there rather than hunting for them elsewhere, you get the version Kalium was tested against.

{% content-ref url="../../getting-started/installation/installing-required-plugins.md" %}
[installing-required-plugins.md](../../getting-started/installation/installing-required-plugins.md)
{% endcontent-ref %}

***

### If a Kalium element is missing

**Portfolio Items isn't there.**\
The portfolio module is switched off at **Kalium -> Settings -> Portfolio**.

**Content Section isn't there.**\
Template Parts is switched off at **Kalium -> Settings -> Template Parts**.

**No Kalium elements at all.**\
The builder plugin may have been installed from somewhere other than **Kalium -> Plugins**, or it needs updating.
