---
description: >-
  The editor built into WordPress, and the Kalium blocks that appear alongside
  the standard ones.
---

# The WordPress Block Editor

The block editor, sometimes called Gutenberg, is built into WordPress. There's nothing to install and nothing to license, and it's what you get by default when you create a new page.

Kalium adds its own blocks to it, so you can drop a portfolio grid or a post listing into a page without any extra plugin.

***

### Kalium's blocks

Add a block, then look for the **Kalium** category in the inserter.

**Portfolio Items**\
A grid of projects with the same layout, column and filtering choices as a portfolio page. Appears only when the portfolio module is enabled under **Kalium -> Settings -> Portfolio**.

**Blog Posts**\
A listing of posts, with control over how many appear, which categories they come from, and how they're laid out.

**Content Section**\
Places a Kalium Template Part of type *Section* into the page. Appears only while Template Parts is enabled.

[TAKE THE SCREENSHOT OF THIS PARTICULAR SECTION AND POST HERE: the block inserter with the Kalium category expanded, showing the three blocks]

***

### These blocks render live

Kalium's blocks aren't fixed snapshots, they ask your site for content each time a page loads.

Publish a new project and it appears in every **Portfolio Items** block automatically. Edit a Template Part and every page using **Content Section** picks up the change. You don't need to go back and re-edit the pages.

***

### Building Template Parts with the block editor

Every Template Part opens in the block editor by default, so you can build a section, header, footer, popup or page replacement here with no extra plugin.

Snippets use the block editor too, in a special form: a single locked code block instead of the usual canvas.

{% content-ref url="../../template-parts/creating-template-parts/" %}
[creating-template-parts](../../template-parts/creating-template-parts/)
{% endcontent-ref %}

***

### Using it alongside a page builder

You can mix builders across a site (some pages in Elementor, some in the block editor) as long as each individual page sticks to one.

If a page was built with WPBakery or Elementor, keep editing it there. Switching a built page to the block editor means rebuilding it.

***

### Common questions

**I don't see a Kalium category in the inserter.**\
Both blocks that can be switched off, Portfolio Items and Content Section, depend on their feature being enabled under **Kalium -> Settings**. If all three are missing, try reloading the editor.

**My block shows "This block has encountered an error".**\
Usually a caching or optimization plugin interfering with the editor. Clear your caches and reload.

**The block looks different on the site than in the editor.**\
Expected to a degree, the editor previews content, but the theme's full styling only applies on the real page. Check the front end before adjusting.
