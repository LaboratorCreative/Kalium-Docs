---
description: >-
  The setting is right, but something else is overriding it. The five usual
  culprits.
---

# A Setting Isn't Working

You've set the option, you've saved, and nothing changed. In almost every case the setting is fine, something else is taking priority over it.

Here are the five things that do that, in the order they're worth checking.

***

### 1. A Template Part has taken over

An active Template Part **replaces** the built-in version on the pages its conditions match. Where a Header part applies, the Customizer's Header screen no longer governs that page at all.

**Check:** open **Kalium -> Template Parts** and look for an active *Header*, *Footer* or *Page* part whose display conditions match the page you're looking at.

**The wrong header shows** where more than one Header part matches the page. Only the first match is used, so tighten one part's conditions.

{% content-ref url="../template-parts/what-are-template-parts.md" %}
[what-are-template-parts.md](../template-parts/what-are-template-parts.md)
{% endcontent-ref %}

***

### 2. A page-builder element has its own settings

**Blog Posts**, **Portfolio Items** and product cards placed as a WPBakery element, an Elementor widget or a block carry **their own settings**. They look like the archive, but they don't read the archive's options.

**The fix:** edit the element itself. The Blog, Portfolio and Product Catalog screens in the Customizer only govern the theme's own archive pages.

{% content-ref url="../other/page-builders/" %}
[page-builders](../other/page-builders/)
{% endcontent-ref %}

***

### 3. A per-page setting is overriding the site setting

If **one** post, page, product or project behaves differently from the rest, open it and scroll to **Parameters and Options**.

Any field set to something other than *Use from Theme Options* wins for that item alone. Set it back to *Use from Theme Options* to hand control back to the Customizer.

{% content-ref url="../other/parameters-and-options.md" %}
[parameters-and-options.md](../other/parameters-and-options.md)
{% endcontent-ref %}

***

### 4. A plugin is missing

Some settings appear whether or not the plugin they need is installed. They simply do nothing without it:

| The setting | Needs |
| --- | --- |
| **Language Switcher** does nothing | WPML active |
| **Breadcrumb** can't be enabled | Breadcrumb NavXT installed |
| The whole **WooCommerce** group is missing | WooCommerce active |
| The **cart** is missing from the header | WooCommerce active, or **Hide when Empty** is on and the cart is empty |
| The **free shipping bar** never appears | A free shipping method with a minimum order set up in WooCommerce, and the page ticked under **Locations to Show** |

***

### 5. The page is stale

The change is saved. You're just not seeing it.

1. **Clear every cache**, hosting, plugin and CDN
2. **Check CSS/JavaScript optimization** isn't serving an older combined file
3. **Load the page signed out**, or in a private browsing window

{% hint style="info" %}
**A change shows in the Customizer preview but not on the live site** is nearly always this. The preview bypasses caching; your visitors don't.
{% endhint %}

***

### Specific cases

#### Project or portfolio URLs return 404

Permalinks need rebuilding after the portfolio slug or its assigned post types change.

Go to **Settings -> Permalinks** and click **Save Changes** once. Nothing needs altering, saving is what rebuilds them.

#### Widgets I deleted are still showing

**Single Post** falls back to **Blog Archive**, and **Single Product** falls back to **Shop Archive**, when the single area is empty. Emptying a widget area doesn't hide the sidebar, it inherits the archive's.

**The fix:** turn the sidebar off for that area instead of emptying it.

{% content-ref url="../general/sidebars/" %}
[sidebars](../general/sidebars/)
{% endcontent-ref %}

#### Template parts appear in search results

They're a post type, so they're searchable by default.

**Customize -> Search Results -> Exclude Post Types** and tick *Template Parts*.

#### Parts of a post are missing whatever I set

Password-protected posts and attachment pages deliberately hide the featured image, author box, share buttons, tags and previous/next links. No setting brings them back on those pages.

#### An Elementor template replaced my archive

Elementor Pro templates whose conditions match an archive address replace Kalium's archive entirely, the same way Kalium's own Template Parts do.

{% content-ref url="plugin-conflicts.md" %}
[plugin-conflicts.md](plugin-conflicts.md)
{% endcontent-ref %}

***

### If a setting has vanished from the screen

That's a different problem. Most Kalium settings are hidden on purpose until a related setting is switched on: **Sticky Effect** only appears once Sticky Header is enabled, and so on.

Check the setting directly above the one you're looking for. If a whole section is missing, check **Kalium -> Settings**, where entire features can be switched off.

{% content-ref url="../getting-started/theme-settings/" %}
[theme-settings](../getting-started/theme-settings/)
{% endcontent-ref %}
