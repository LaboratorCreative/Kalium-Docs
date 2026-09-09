---
description: >-
  Bundled plugin updates, double lightboxes, caching plugins, and finding which
  two plugins don't get along.
---

# Plugin Problems and Conflicts

Kalium bundles four premium plugins — **ACF Pro**, **WPBakery Page Builder**, **Slider Revolution** and **LayerSlider**. They're licensed through your Kalium license, so you install and update them from **Kalium -> Plugins**, not the usual WordPress plugin screen.

Two things follow from that, and between them they explain most plugin problems: **the theme supplies the download**, and **an inactive license means no downloads at all**.

***

## Bundled plugin problems

### "Update package not available"

By far the most common — usually on ACF Pro or Slider Revolution.

The plugin author has released a new version, but WordPress has nowhere to download it from, because a bundled premium plugin has no public download. Kalium supplies the file, and it can only supply a version it actually carries.

**Check first:**

1. **Kalium -> Status** — is your license active? An inactive license means no plugin downloads.
2. **Kalium -> Status** — is the theme itself up to date? A newer bundled plugin usually arrives *with* a theme update.

**The fix:**

1. **Update Kalium first**
2. Then open **Kalium -> Plugins** and update the plugin from there

{% hint style="warning" %}
**If it still won't update**, the plugin author has released a version newer than the one your Kalium version carries. Wait for the next Kalium release, which will bundle it.

**Don't download the plugin from anywhere else.** A copy from elsewhere won't match your license and will be overwritten.
{% endhint %}

***

### WPBakery is asking for a license key

The bundled copy is licensed through Kalium and should never need its own key. Being asked for one means it was installed from somewhere else, or your Kalium license is inactive.

**Check** **Kalium -> Status** for an active license, then reinstall WPBakery from **Kalium -> Plugins**.

***

### Portfolio pages show a critical error

Almost always **ACF Pro being inactive**. The portfolio's per-project fields are ACF fields, so without it the project template has nothing to render.

1. **Plugins -> Installed Plugins** — check *Advanced Custom Fields PRO* is active
2. If it isn't installed, get it from **Kalium -> Plugins**
3. Reload a project page

***

### My widgets disappeared

WordPress replaced the classic widget screen with a block-based one. Your sidebars still exist — the new screen just may not show them as you expect.

1. Install and activate the **Classic Widgets** plugin
2. Open **Appearance -> Widgets** — your sidebars and their content are there

{% content-ref url="../general/sidebars/troubleshooting-sidebar.md" %}
[troubleshooting-sidebar.md](../general/sidebars/troubleshooting-sidebar.md)
{% endcontent-ref %}

***

## Finding a conflict

A conflict is when two things work on their own but not together. The method is always the same.

1. **Note exactly what's broken** and how to reproduce it
2. **Deactivate all plugins** except the ones Kalium requires
3. **Test.** If the problem is gone, reactivate plugins **one at a time**, testing after each
4. The plugin that brings the problem back is one half of the pair

Do this on a staging copy if you have one.

***

### Caching and optimization plugins

**The most frequent conflict of all.** Combining or deferring the theme's JavaScript breaks menus, sliders and galleries.

1. Switch off **minify JS**, **combine JS** and **delay JavaScript execution**
2. Clear all caches and test
3. Re-enable them one at a time, testing after each

**If you need those settings on**, exclude Kalium's own scripts from optimization. Most plugins accept a path pattern — exclude anything under the theme's `assets/js` directory.

***

### Two lightboxes open at once

A gallery plugin is applying its own lightbox on top of Kalium's.

**Either** disable the other plugin's lightbox while keeping its linking behavior, **or** turn Kalium's off at **Appearance -> Customize -> General -> Lightbox** and let the other plugin own it.

Either works — just don't have both.

{% content-ref url="../other/lightbox.md" %}
[lightbox.md](../other/lightbox.md)
{% endcontent-ref %}

***

### My header and footer disappeared after activating Elementor Pro

Elementor Pro's Theme Builder takes over headers and footers as soon as it's active, even if you haven't built one.

**Either** build a header and footer in Elementor's Theme Builder, **or** let Kalium handle them — Kalium restores its own when no Elementor header or footer matches the page. If both are missing, update Kalium.

***

### An Elementor template replaced my portfolio archive

An Elementor template whose display conditions match the portfolio address replaces Kalium's archive entirely.

Narrow that template's conditions so it no longer matches, or accept it and build the listing in Elementor.

***

### A page builder can't edit a portfolio or archive page

Archives are generated by the theme rather than stored as page content, so a builder has nothing to open.

To design that layout, create a **Template Part** of type *Page* with conditions targeting the archive. That gives the builder a real canvas to work on.

{% content-ref url="../template-parts/creating-template-parts/replace-a-page.md" %}
[replace-a-page.md](../template-parts/creating-template-parts/replace-a-page.md)
{% endcontent-ref %}

***

### Custom CSS is being ignored

Usually specificity rather than a conflict.

**Check** **Appearance -> Customize -> Additional CSS** and your child theme's stylesheet for existing rules using `!important` on the same property.

**The fix:** remove the competing `!important`, or make your own selector more specific. Better still, set the value through the Customizer where one exists — it survives updates and avoids the fight entirely.

***

### A slider doesn't appear

1. Is the slider plugin active?
2. Does the slider have at least one **published** slide?
3. Is a caching plugin combining or deferring JavaScript? Sliders are script-driven and are frequently broken by it.

***

### A plugin update broke the site

1. Access your site by FTP and rename the plugin's folder in `wp-content/plugins/` to disable it
2. Reload to confirm the site recovers
3. If it was one of the four bundled plugins, reinstall it through **Kalium -> Plugins** — that copy matches what the theme expects

{% content-ref url="critical-errors.md" %}
[critical-errors.md](critical-errors.md)
{% endcontent-ref %}

***

### Kalium's blocks are missing from the inserter

**Portfolio Items** appears only when the portfolio module is enabled, and **Content Section** only when Template Parts is enabled. Both are under **Kalium -> Settings**.

{% content-ref url="../getting-started/theme-settings/" %}
[theme-settings](../getting-started/theme-settings/)
{% endcontent-ref %}
