---
description: >-
  The builder bundled with Kalium, and the 27 elements the theme adds to it.
---

# WPBakery

WPBakery Page Builder is bundled with Kalium. It's included with your theme license, so there's nothing extra to buy and no separate key to enter.

Most of Kalium's starter sites are built with WPBakery, so if you imported one, this is very likely the builder your pages already use.

Install it from **Kalium -> Plugins**.

{% hint style="info" %}
**You don't need to activate WPBakery separately.** It's licensed through Kalium. If you see a prompt asking for a WPBakery purchase code, you can ignore it, the theme handles the licensing.
{% endhint %}

***

### Kalium's elements

Kalium adds **27 elements** to WPBakery. They appear alongside the standard ones when you add an element to a row.

[TAKE THE SCREENSHOT OF THIS PARTICULAR SECTION AND POST HERE: the WPBakery element picker showing the Kalium elements]

**Content**

| Element | What it does |
| --- | --- |
| **Heading** | A styled heading with size and alignment control |
| **Button** | A button using your theme's button styles |
| **Alert Box** | A colored message box |
| **Divider** | A horizontal separator |
| **Auto Type** | Text that types itself out, cycling through phrases |
| **Placeholder** | Blank spacing while you lay a page out |
| **Scroll Box** | A scrollable area within the page |

**Listings**

| Element | What it does |
| --- | --- |
| **Portfolio** | A grid of projects |
| **Masonry Portfolio** | A masonry-style project grid |
| **Portfolio Item** | A single hand-picked project |
| **Blog Posts** | A listing of posts |
| **Products Carousel** | A sliding row of WooCommerce products |
| **Dribbble Gallery** | Shots pulled from a Dribbble account |

**People and services**

| Element | What it does |
| --- | --- |
| **Team Members** / **Team Member** | A team grid, and one person within it |
| **Clients** / **Client Logo** | A logo strip, and one logo within it |
| **Service Box** / **Service Content** | Service listings |
| **Pricing Table** | A pricing plan column |

**Site pieces**

| Element | What it does |
| --- | --- |
| **Content Section** | Places a Kalium Template Part of type *Section* |
| **Contact Form** | A contact form |
| **Map** / **Map Location** | A Google map, and a pin within it |
| **Social Networks** | Your social icons |
| **Like + Share** | Like and share buttons |
| **Breadcrumb** | The breadcrumb trail |

{% hint style="info" %}
Elements that come in pairs (**Team Members** and **Team Member**, **Clients** and **Client Logo**, **Map** and **Map Location**) work together. Add the container first, then add the individual items inside it.
{% endhint %}

***

### Google Maps needs an API key

The **Map** element needs a Google Maps API key before it will display anything. Add yours under **Appearance -> Customize -> General**.

Without a key, Google shows a gray box with a warning instead of your map.

***

### Building Template Parts with WPBakery

Template Parts of type *Section*, *Header*, *Footer*, *Page* and *Popup* can all be built with WPBakery.

{% content-ref url="../../template-parts/creating-template-parts/creating-a-section/creating-a-section-with-wpbakery.md" %}
[creating-a-section-with-wpbakery.md](../../template-parts/creating-template-parts/creating-a-section/creating-a-section-with-wpbakery.md)
{% endcontent-ref %}

***

### Common questions

**The Portfolio elements are missing.**\
The portfolio module is off under **Kalium -> Settings -> Portfolio**.

**Content Section is missing.**\
Template Parts is off under **Kalium -> Settings -> Template Parts**.

**WPBakery is asking for a purchase code.**\
Ignore it, the theme licenses it for you.

**My page shows shortcodes as plain text like `[vc_row]`.**\
WPBakery has been deactivated. Reinstall it from **Kalium -> Plugins** and the page renders again, the content is safe, it just needs the plugin to display it.

**The map is a gray box.**\
Add a Google Maps API key under **Appearance -> Customize -> General**.
