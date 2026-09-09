---
description: White screens, PHP errors, and getting back into a site you can't reach.
---

# Critical Errors and Blank Pages

A white screen, or the message "There has been a critical error on this website", means PHP stopped running. The message alone almost never says why, so the job is to narrow it down quickly.

**None of this deletes anything.** Everything below is reversible.

***

### First: find out what the error actually says

WordPress hides the details from visitors by default. Turning the log on takes a minute and usually names the exact file and line.

Add these two lines to `wp-config.php`, above the line that says `/* That's all, stop editing! */`:

```php
define( 'WP_DEBUG', true );
define( 'WP_DEBUG_LOG', true );
```

Reload the page that fails, then open `wp-content/debug.log`. The last entries name the cause.

{% hint style="warning" %}
**Remove these lines when you're done.** Leaving debugging on can expose information about your site to visitors.
{% endhint %}

Also check **Kalium -> Status** if you can reach your admin: Kalium needs **PHP 7.4 or newer** and **at least 128 MB of memory**.

***

### The whole site is down

You'll need FTP access or your host's file manager for this.

**Step 1 — rule out plugins**

1. Rename the folder `wp-content/plugins` to `plugins-off`
2. Reload your site

**If the site comes back**, a plugin is the cause. Rename the folder back to `plugins`, then go to **Plugins** in your admin and disable them one at a time until the problem returns.

**Step 2 — rule out the theme**

If the site is still down:

1. Rename `wp-content/themes/kalium` to `kalium-old`
2. Download a fresh copy of the theme from your Laborator account
3. Upload it as `kalium`
4. Reload

{% hint style="info" %}
Renaming the plugins folder disables everything at once — it's the fastest way to answer "is it a plugin?" Nothing is lost; your settings are all in the database and come back when you rename the folder.
{% endhint %}

***

### The site works but I can't reach the admin

1. Disable all plugins by renaming `wp-content/plugins` over FTP
2. Log in
3. Rename the folder back and reactivate plugins one at a time

**If that doesn't work**, rename the Kalium folder so WordPress falls back to a default theme, log in, then reinstall Kalium from your account.

{% hint style="info" %}
**If a code snippet is the cause**, there's a faster way in. Add this to `wp-config.php`:

```php
define( 'KALIUM_SNIPPETS_SAFE_MODE', true );
```

Every snippet stops running and your admin is reachable again. Remove the line once you've fixed the snippet.
{% endhint %}

{% content-ref url="../template-parts/creating-template-parts/code-snippets/troubleshooting-snippets.md" %}
[troubleshooting-snippets.md](../template-parts/creating-template-parts/code-snippets/troubleshooting-snippets.md)
{% endcontent-ref %}

***

### One page is blank but the rest of the site works

This is rarely a real error — usually something is deliberately replacing that page.

**Check first:**

1. **Is a Template Part replacing it?** Open **Kalium -> Template Parts** and look for a *Page* type whose display conditions match that page.
2. **Was the page built with a page builder that's now inactive?** A page built in WPBakery or Elementor shows nothing if the plugin is disabled.

Disable the matching template part, or reactivate the builder plugin, and reload.

{% content-ref url="settings-not-applying.md" %}
[settings-not-applying.md](settings-not-applying.md)
{% endcontent-ref %}

***

### Only the portfolio breaks

This is Advanced Custom Fields Pro being inactive, in almost every case.

ACF Pro is bundled with Kalium and powers the portfolio's settings. Install and activate it from **Kalium -> Plugins**.

{% content-ref url="plugin-conflicts.md" %}
[plugin-conflicts.md](plugin-conflicts.md)
{% endcontent-ref %}

***

### PHP version errors

An error mentioning a PHP version, or a `TypeError`, usually means your host upgraded PHP underneath you.

1. Check **Kalium -> Status** for your PHP version
2. Update Kalium and all its bundled plugins — the latest versions carry the compatibility fixes
3. If the site is down and you can't reach the admin, ask your host to move PHP back one version temporarily, then update

***

### If you get the site back

Once it's running again, work out what caused it before carrying on:

* **A plugin** — check whether it has an update, or find an alternative
* **A code snippet** — check the Template Parts list for one showing an **Error** status
* **The update didn't finish** — check **Kalium -> Status** shows the version you expect
* **Server limits** — ask your host to raise the memory limit to 256 MB

{% content-ref url="bad-hosting-environment.md" %}
[bad-hosting-environment.md](bad-hosting-environment.md)
{% endcontent-ref %}
