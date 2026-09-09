---
description: >-
  The list won't load, the import stops partway, images are missing, or the
  result doesn't match the demo.
---

# Starter Site Import Problems

Importing a starter site asks a lot of a server in one go — it creates hundreds of pages, downloads hundreds of images and installs several plugins. Almost every problem comes down to one of three things: **server limits**, **an inactive license**, or **a theme version older than the fix**.

{% hint style="info" %}
**Before anything else, make sure Kalium is up to date.** Importer problems were fixed in several releases, and on WordPress 7.1 specifically, versions before Kalium 4.7 cannot import at all.
{% endhint %}

***

### The starter sites list is empty or won't load

The list is fetched from Laborator when you open the screen, so it needs two things to work.

**Check first:**

1. **Kalium -> Status** — is your license active? The list needs one.
2. Can your server reach the internet? The Status screen runs connection tests and will tell you.

**The fix:** activate your license, then reload the page. If the connection tests fail, ask your host to allow outbound HTTPS connections.

{% content-ref url="license-and-activation.md" %}
[license-and-activation.md](license-and-activation.md)
{% endcontent-ref %}

***

### The import stops partway

This is nearly always PHP memory or execution time running out.

**Check first:** open **Kalium -> Status** and look at your memory limit. It should be **at least 128 MB**, and image-heavy starter sites need more — some sites have needed 756 MB before the import would finish.

**The fix:**

1. Ask your host to raise the PHP memory limit, and `max_execution_time` along with it
2. Run the import again — **it resumes rather than starting over**, so nothing is repeated
3. If it keeps stalling, import the media separately. It's by far the slowest step.

{% hint style="warning" %}
**Don't run a second import on top of a half-finished one.** Remove the starter site content first, then import again cleanly. Layering imports leaves duplicated content that's tedious to untangle.
{% endhint %}

***

### A fatal error during import

Errors like `TypeError in in_array()`, a missing `Import_Type` class, or a JSON error from the options file are **version bugs, not configuration problems**.

Update Kalium to the latest version and try again. The importer was fixed in several releases, and running an old version against a newer WordPress is the usual cause.

***

### Images are missing after the import

Media is imported last and takes the longest, so a stall during that step leaves you with all the content and none of the pictures.

**Check first:** did the import report that it completed? If it stopped during media, that's your answer.

**The fix:** run the import again, selecting only the media step.

If images still fail, your server may be unable to reach Laborator's media server — some hosts and some regions block it. Contact support and they can supply the files for a manual import.

***

### The import worked but the site doesn't match the demo

**Check first:**

1. **Is the right page builder active?** Each starter site is built for one — WPBakery, Elementor or the block editor — and the demo won't look right without it.
2. **Did every plugin install?** The importer installs and activates the plugins a starter site needs, including bundled ones like Slider Revolution. A plugin missing afterwards means its task failed, not that you missed a step.

**The fix:** run the import again. Steps that completed are skipped, and the failed plugin is retried.

If the plugin fails again, check **Kalium -> Status**. **Bundled premium plugins can't download without an active license**, and that's usually what stops the task.

{% content-ref url="../getting-started/installation/importing-a-starter-site.md" %}
[importing-a-starter-site.md](../getting-started/installation/importing-a-starter-site.md)
{% endcontent-ref %}

***

### Importing settings exported from another site fails

The options file carries a version number, and **an export from a newer Kalium won't import into an older one**.

Update both sites to the same version, then export and import again.

{% content-ref url="manage-options-in-customizer.md" %}
[manage-options-in-customizer.md](manage-options-in-customizer.md)
{% endcontent-ref %}

***

### Giving the import the best chance

If you're about to import and want it to go smoothly:

* **Import into a fresh WordPress install** where possible. Starter sites are designed for that, and it avoids clashing with content you already have.
* **Ask your host to raise the memory limit** to 256 MB before you start.
* **Make sure your license is active** — several steps depend on it.
* **Don't close the tab** while it runs.
* **Import on a staging site first** if you have one, especially on a live site with real content.

{% content-ref url="../wp-cli-api/starter-sites.md" %}
[starter-sites.md](../wp-cli-api/starter-sites.md)
{% endcontent-ref %}
