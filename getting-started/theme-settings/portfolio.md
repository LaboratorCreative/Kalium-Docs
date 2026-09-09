---
description: >-
  Turn the portfolio module on or off, and give its layouts to any post type on
  your site.
---

# Portfolio Settings

**Kalium -> Settings -> Portfolio** controls the portfolio module: whether it's loaded at all, and — since Kalium 4.7 — which post types get to use it.

***

### Portfolio Extension

**On by default.**

This loads the portfolio module — the Portfolio post type, its project layouts, its Customizer screens and its builder elements.

Turning it off removes all of that. If you're building a shop or a blog and have no use for a portfolio, switching it off keeps your Customizer tidier. Nothing is deleted; your projects stay in the database.

{% hint style="info" %}
**"My Portfolio options disappeared from the Customizer."** This setting is the usual reason.
{% endhint %}

***

### Portfolio Post Types

This is the setting worth knowing about, and it's easy to miss.

**The portfolio module is not tied to the Portfolio post type.** Tick any public post type in this list and it gains the entire module — the same layouts, galleries and options that Portfolio has.

That's how a **Case Studies**, **Services** or **Projects** post type gets Kalium's project layouts without being called Portfolio.

A ticked post type receives:

* **Its taxonomies attached automatically**, so filtering works
* **Its own complete set of Portfolio options in the Customizer**, named after the post type
* **The Parameters and Options panel** on its items — Project Layout, Project Gallery, Checklists and the rest
* **Its own Preselected Item Type and Default Archive Page** (below)

***

### Per-post-type settings

For **each** post type you tick, two more settings appear, named after it:

**Preselected Item Type**\
The project layout new items start on. If most of your case studies use the same layout, set it here and stop choosing it every time.

**Default Archive Page**\
The page used as that post type's archive — the listing visitors see.

***

### Adding a post type

1. Tick it under **Portfolio Post Types**
2. Save
3. Its Customizer screens appear right away

{% hint style="warning" %}
**If the new options don't show in the Customizer**, save this settings page and then reload the Customizer. The screens are registered on the next load.

**If project URLs return a 404 error** after adding or removing a post type, go to **Settings -> Permalinks** and click Save once. Nothing needs changing — saving is what rebuilds the URLs.
{% endhint %}

***

### Removing a post type

Untick it and save.

The post type keeps all its posts and goes back to its own templates. It simply stops using the portfolio module, and its Portfolio option screens disappear.

**Your settings are kept**, so ticking it again restores everything as it was.

***

### Turning the portfolio off entirely

Switch **Portfolio Extension** off. Nothing is deleted — the module just stops loading.

{% content-ref url="../../post-types/portfolio/" %}
[portfolio](../../post-types/portfolio/)
{% endcontent-ref %}
