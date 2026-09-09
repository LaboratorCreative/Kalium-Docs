---
description: Broken layouts, missing images, lost settings and failed updates.
---

# Problems After Updating

The most common category of support request, and almost all of it comes down to four causes: a cache still serving old files, a plugin that needs updating alongside the theme, settings stored somewhere the update didn't touch, or an optimization plugin rewriting the theme's code.

***

### Check these first, in order

Most problems on this page are solved before you reach the specific sections below.

1. **Clear every cache**, your caching plugin, your host's cache, and any CDN such as Cloudflare. Then hard refresh (**Ctrl+Shift+R** / **Cmd+Shift+R**).
2. **Update the plugins too.** **Kalium -> Plugins**, update anything with a newer version. A theme update often expects newer plugins.
3. **Check the update finished.** **Kalium -> Status**, does the theme version match what you expected? A failed update can leave a half-written theme folder.
4. **Turn off CSS/JS optimization** temporarily, minify, combine and delay JavaScript. Reload. If that fixes it, re-enable one setting at a time to find which.

***

### A critical error right after updating

The update didn't complete, or a plugin is now incompatible.

**To reinstall the theme cleanly:**

1. Connect by FTP or open your host's file manager
2. Rename `wp-content/themes/kalium` to `kalium-old`
3. Download a fresh copy of the theme from your Laborator account
4. Upload it as `kalium`
5. Reload the site, then clear all caches

**If that doesn't work**, the cause is a plugin. Rename `wp-content/plugins` to `plugins-off` to disable everything at once. If the site comes back, rename the folder back and disable plugins one at a time until you find it.

{% content-ref url="critical-errors.md" %}
[critical-errors.md](critical-errors.md)
{% endcontent-ref %}

***

### Images disappeared or show as broken

Usually a cache serving old markup, or a site move that left image addresses pointing at the old domain.

**Check first:** open a broken image in a new tab and look at its address. If it contains an old or staging domain, the problem is the address, not the theme.

**If the addresses are wrong**, run a search-and-replace across the database for the old domain. Your host can do this, or a migration plugin.

**If the addresses are right** but images still fail, regenerate your thumbnails.

{% content-ref url="image-problems.md" %}
[image-problems.md](image-problems.md)
{% endcontent-ref %}

***

### My theme settings are gone after moving the site

Theme settings are stored in the database per site, so they don't travel with a copy of your files.

**To move them properly:**

1. On the original site, go to **Appearance -> Customize -> Manage Options** and export
2. On the new site, open the same screen and import the file you downloaded

Every Customizer setting is restored. Fonts, template parts and portfolio content are stored separately and travel with the database.

{% content-ref url="manage-options-in-customizer.md" %}
[manage-options-in-customizer.md](manage-options-in-customizer.md)
{% endcontent-ref %}

***

### Fonts reverted to a default after upgrading to Kalium 4

Kalium 4 moved typography out of the Customizer into its own screen.

1. Open **Kalium -> Typography**
2. Check your fonts are listed and active, re-add any that are missing
3. Clear your caches

{% content-ref url="../typography/fonts/" %}
[fonts](../typography/fonts/)
{% endcontent-ref %}

***

### Layout or spacing changed after upgrading from Kalium 3

Kalium 4 rebuilt the styling system, and some Kalium 3 values don't carry across, particularly custom CSS written against the old class names.

**Check first:** open **Appearance -> Customize -> Additional CSS** and look for rules using `!important`. These often survive an upgrade and then fight the new defaults. Check your child theme's stylesheet too.

**The fix** is to remove or rewrite those rules, then set the same value through the Customizer instead, so it survives future updates.

{% content-ref url="../getting-started/migrating-from-kalium-3-to-4/" %}
[migrating-from-kalium-3-to-4](../getting-started/migrating-from-kalium-3-to-4/)
{% endcontent-ref %}

***

### The mobile menu stopped working

Almost always an optimization plugin deferring or combining the theme's JavaScript.

1. In your optimization plugin, switch off **delay JavaScript execution** and **combine JavaScript**
2. Clear caches and test on a real phone, not just a narrow browser window
3. Re-enable the settings one at a time, testing the menu after each

***

### The update times out, or returns a 503 error

The update is exceeding your server's limits.

**Check first:** **Kalium -> Status**, and look at *Memory Limit* and *Max Execution Time*. Kalium expects at least **128 MB** and **PHP 7.4** or newer.

**The fix:**

1. Ask your host to raise the memory limit to 256 MB and max execution time to 120 seconds
2. Try the update again
3. If it still fails, update by FTP instead, download the theme from your account and upload it manually

{% content-ref url="../getting-started/installation/installing-theme-via-ftp.md" %}
[installing-theme-via-ftp.md](../getting-started/installation/installing-theme-via-ftp.md)
{% endcontent-ref %}

***

### WPBakery elements are missing after an update

Kalium's elements are registered by the theme, so an outdated theme can lose them even when WPBakery itself is up to date.

**Update Kalium first**, then WPBakery from **Kalium -> Plugins**.

***

### Spacing or margins changed after updating WPBakery

Clear every cache first. This is usually all it takes.

If it persists, check whether your custom CSS targets WPBakery's own class names. Those change between major versions, so a rule that worked before may now be pointing at nothing.
