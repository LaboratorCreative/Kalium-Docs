---
description: >-
  The tabbed panel below the editor, where you override the site-wide settings
  for one page, post, project or product.
---

# Parameters and Options

The Customizer sets how your whole site looks. **Parameters and Options** is where you change that for **one** piece of content — hide the footer on a single landing page, use a different logo on the contact page, give one blog post a full-width featured image.

**Where to find it:** edit any post, page, portfolio item or product, then scroll **below** the content editor to the box titled **Parameters and Options**.

***

### How the panel behaves

Three things about this panel confuse people, and all three are by design.

**Tabs appear and disappear.** A tab only shows when it applies — the right post type, the right post format, the right project layout. This is why the panel looks completely different on a blog post than on a portfolio item, and why changing one dropdown can make new tabs appear.

**"Use from Theme Options" means the Customizer decides.** Almost every dropdown starts there (sometimes worded *Inherit from Theme Options*). Choose anything else and this one item overrides the site-wide setting. To go back, set it to *Use from Theme Options* again.

{% hint style="info" %}
For dropdowns, clearing a field is **not** the same as choosing *Use from Theme Options*. For color and spacing fields, though, an empty value does mean "inherit" — so you can override one color and leave the rest alone.
{% endhint %}

**Your last tab is remembered.** Reopen the same item and the panel returns to where you left it.

***

### Which tabs appear where

| Tab | Post | Page | Portfolio item | Product |
| --- | :---: | :---: | :---: | :---: |
| **Page Options** | Yes | Yes | Yes | Yes |
| **Custom CSS** | Yes | Yes | Yes | Yes |
| **Post Settings** | Yes | | | |
| **Video / Audio / Gallery settings** | by format | | | |
| **Portfolio Settings** | | template only | | |
| **Project Layout** | | | Yes | |
| **General Details** | | | Yes | |
| **Featured Video** | | | Yes | |
| **Other Settings** | | | Yes | |
| **Project Link, Checklists, Project Gallery** | | | by layout | |

{% hint style="warning" %}
**Portfolio Settings catches everyone out.** It appears on a **page** — one using the Portfolio page template — not on a portfolio item. It configures the listing, not an individual project.
{% endhint %}

***

## Page Options

Available on everything. These settings are about the **frame** around your content — the header, the footer, the heading, the container width — rather than the content itself.

### Header Options

**Header Position**\
*Use from Theme Options* · *Content Below (Static)* · *Over the Content (Absolute)*. Choosing *Over the Content* makes the header transparent and sits it on top of the page, which is what you want when a page opens with a full-width image.

**Header Spacing**\
Only appears when the position is *Over the Content*. Sets how much room to leave so your content isn't hidden behind the header.

**Full-width Header**\
Extends the header to the edges of the browser window on this page.

**Header Styling**\
Set this to *Yes* and a complete set of color overrides appears for this page alone — background, borders, padding, text, submenu colors, mobile menu colors, and separate normal / hover / active colors for links and menu pills.

**Empty values are ignored**, so you can override a single color and leave everything else as it is.

{% content-ref url="../general/header/in-page-options.md" %}
[in-page-options.md](../general/header/in-page-options.md)
{% endcontent-ref %}

### Heading Title

Controls the title area at the top of the page.

**Heading Title**\
On or off. The rest of the tab only appears when it's on.

**Page Title Type**\
*Show this post title* or *Enter custom title* — useful when the page's real title is long and you want something shorter on screen.

**Page Heading Description Type**\
*Use this post description* or *Enter custom description*.

### Logo & Menu

**Custom Logo** and **Custom Logo Width**\
A different logo on this page. The width is the maximum in pixels, which matters if you upload a retina (@2x) image.

**Sticky Header**\
*Use from Theme Options* · *Enable* · *Disable*. This is how you turn the sticky header off on one page.

**Custom Sticky Logo**\
A different logo for when the header is stuck to the top.

**Sticky Header Style**\
Appears when sticky is set to *Enable* — a full set of color and spacing overrides for the sticky state on this page.

### Footer Options

**Footer Visibility**\
*Use from Theme Options* · *Show footer on this page* · *Hide footer on this page*. This is how you hide the footer on a landing page.

**Fixed Footer**\
*Use from Theme Options* · *Normal* · three *Fixed to Bottom* variants with different animations.

### Other Options

**Custom Container Width**\
Turn this on to set a different content width for this page. It reveals **Container Width** — *Large*, *Medium*, *Small* or *Custom* — and a slider when you pick *Custom*.

**Fullwidth container**\
Overrides the width entirely and runs the content edge to edge.

### Breadcrumb

**Breadcrumb**\
*Inherit from Theme Options* · *Enable* · *Disable*. Everything below appears only when set to *Enable*.

The rest — background and text color, border type and color, radius, margins and alignment — overrides the site-wide breadcrumb styling for this page. Leave a color empty to inherit it.

{% hint style="info" %}
Breadcrumbs need the **Breadcrumb NavXT** plugin. Without it these fields do nothing. See [Breadcrumbs](breadcrumbs.md).
{% endhint %}

***

## Custom CSS

**Custom Page Style**\
CSS that applies to this item only. Don't wrap it in `<style>` tags — just the CSS itself.

Good for a one-off tweak on a single page. For anything you'll reuse, a CSS snippet or Additional CSS is a better home.

{% content-ref url="custom-css.md" %}
[custom-css.md](custom-css.md)
{% endcontent-ref %}

***

## Post Settings

On blog posts only.

**Featured Image Placing**\
*Use from Theme Options* · *Boxed* · *Wide* · *Full Width* · *Hide Featured Image*. This is how one post gets a full-width header image when the rest are boxed.

**Image Size**\
*Use from Theme Options* · *Default Thumbnail Size* · *Original Image Size*. Hidden when the image is set to be hidden.

**Show Related Posts**\
*Inherit from Theme Options* · Show · Hide.

{% hint style="info" %}
The Show Related Posts options read "Products" on screen. On a blog post they control related **posts** — it's a wording slip in the theme, not a sign you're on the wrong setting.
{% endhint %}

### Tabs that depend on the post format

Set the post **Format** first, and a matching tab appears:

| Format | Tab | What's in it |
| --- | --- | --- |
| Video | **Video Post Settings** | Video Resolution, Auto Play Video |
| Audio | **Audio Post Settings** | Auto Play Audio |
| Gallery | **Post Slider Images** | The gallery images |

***

## Portfolio item tabs

Portfolio items have the most settings, because the project layouts differ so much from one another.

**Project Layout -> Item Type** is the first choice, and it decides what else you see: *Side Portfolio*, *Columned*, *Carousel*, *Zig Zag*, *Fullscreen*, *Lightbox* or *Design Your Own*.

{% hint style="warning" %}
**Change the Item Type, then click Update.** The tabs for the new type won't appear until you save.
{% endhint %}

The remaining tabs are:

**General Details** — a sub-title under the project title, and custom previous/next navigation.

**Featured Video** — replaces the featured image with a video. Autoplay is muted automatically.

**Other Settings** — hover colors and effects for this project's thumbnail in the grid.

**Project Link** — the "Launch website" button and where the thumbnail leads.

**Checklists** — lists of details shown alongside the project.

**Project Gallery** — the project's images, videos, sliders, comparisons and quotes.

Each layout is covered in full in its own article:

{% content-ref url="../post-types/portfolio/creating-a-portfolio-item/" %}
[creating-a-portfolio-item](../post-types/portfolio/creating-a-portfolio-item/)
{% endcontent-ref %}

{% hint style="info" %}
**Lightbox items** have no Project Link, Checklists or Project Gallery tabs — they never open a page, so everything is set on the Lightbox tab itself.

**Design Your Own** has no layout tab at all — you build that one with the page builder.
{% endhint %}

***

## Portfolio Settings — on a page

This tab appears on a **page** using the **Portfolio** page template, and it configures the listing: how many columns, which items appear, the hover effect, whether it's a masonry grid.

{% content-ref url="../post-types/portfolio/creating-a-portfolio-page.md" %}
[creating-a-portfolio-page.md](../post-types/portfolio/creating-a-portfolio-page.md)
{% endcontent-ref %}

***

### When a tab is missing

**The whole panel is missing.**\
Advanced Custom Fields Pro powers this panel and must be active. It's bundled with Kalium — install it from **Kalium -> Plugins**.

**You changed Item Type and nothing appeared.**\
Click **Update** first.

**You're looking for portfolio listing settings on a project.**\
They're on the **page** that uses the Portfolio template.

**The format tabs aren't showing on a post.**\
Set the post **Format** first.

**The Breadcrumb fields are grayed out.**\
Breadcrumb NavXT isn't installed, or Breadcrumb isn't set to *Enable*.
