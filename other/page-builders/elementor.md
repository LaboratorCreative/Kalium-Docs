---
description: What Kalium adds to Elementor, and how the two work together.
---

# Elementor

Elementor is a visual page builder, you drag elements onto the page and see the result as you work. Kalium supports it fully and adds three of its own widgets, plus a few connections that make the theme and the builder agree with each other.

Install it from **Kalium -> Plugins** so you get the version Kalium was tested against.

***

### Kalium's widgets

Open the widget panel in Elementor and search for these:

**Portfolio Items**\
A grid of projects with the same layout, column and filtering choices as a portfolio page. Only appears when the portfolio module is enabled under **Kalium -> Settings -> Portfolio**.

**Blog Posts**\
A listing of posts, with control over how many appear, which categories they come from, and how they're laid out.

**Content Section**\
Places a Kalium Template Part of type *Section* into the page. Only appears while Template Parts is enabled.

[TAKE THE SCREENSHOT OF THIS PARTICULAR SECTION AND POST HERE: the Elementor widget panel with the Kalium widgets visible]

***

### Your Kalium fonts appear in Elementor

Any font you've added under **Kalium -> Typography** shows up in Elementor's own font picker, listed alongside Google Fonts and the system ones.

That means you set a font up once, in one place, and use it in both. You don't need to add it again for Elementor.

{% content-ref url="../../typography/fonts/" %}
[fonts](../../typography/fonts/)
{% endcontent-ref %}

***

### Your Kalium colors appear in Elementor

The palette you set under **Appearance -> Customize -> Styling -> Colors** is available in Elementor as global colors.

Pick a color from the palette rather than typing a hex value, and changing the palette later updates everything at once.

{% content-ref url="../../styling/colors.md" %}
[colors.md](../../styling/colors.md)
{% endcontent-ref %}

***

### Building Template Parts with Elementor

Kalium's Template Parts can be built with Elementor, sections, headers, footers, popups and page replacements all open in Elementor's full editor, the same as a normal page.

The one exception is **Snippets**, which hold code rather than layout. Elementor isn't offered for those.

{% content-ref url="../../template-parts/creating-template-parts/creating-a-section/creating-a-section-with-elementor.md" %}
[creating-a-section-with-elementor.md](../../template-parts/creating-template-parts/creating-a-section/creating-a-section-with-elementor.md)
{% endcontent-ref %}

***

### Elementor Pro's Theme Builder

If you have Elementor Pro, you have two ways to replace a header, footer or archive template, Elementor's Theme Builder, and Kalium's Template Parts. Both work.

**Pick one and stick to it.** Using both to replace the same thing is where problems start: two headers on a page almost always means one of each is active.

{% hint style="info" %}
**A Kalium setting stopped working after building with Elementor Pro's Theme Builder.** An Elementor template is replacing that part of the page, so the Customizer no longer governs it. Same as with Kalium's own Template Parts, whichever replaces the header owns the header.
{% endhint %}

***

### Common questions

**A Kalium widget is missing from the panel.**\
Portfolio Items needs the portfolio module enabled; Content Section needs Template Parts enabled. Both are under **Kalium -> Settings**.

**My theme fonts don't appear in Elementor's picker.**\
Check the font is saved under **Kalium -> Typography** and reload the editor.

**The page looks different in the editor than on the site.**\
Usually caching. Clear your caching plugin and reload.

**I can't edit a portfolio archive with Elementor.**\
Archives aren't normal pages, so a builder can't open them directly. Use a Template Part of type *Page* instead.

{% content-ref url="../../template-parts/creating-template-parts/replace-a-page.md" %}
[replace-a-page.md](../../template-parts/creating-template-parts/replace-a-page.md)
{% endcontent-ref %}
