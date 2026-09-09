---
description: >-
  Replace Kalium's branding in the admin with your own, for agencies handing a
  site to a client.
---

# White Label

**Kalium -> Settings -> White Label** replaces Kalium's branding throughout the WordPress admin with your own, and hides the dashboard pages that reveal which theme the site is built on.

This is built for agencies. If you build sites for clients and would rather the admin say your studio's name than Kalium's, this is the section for it.

{% hint style="info" %}
**This section only appears if your license includes the White Label feature.** If you can't see it in the settings navigation, that's why. See [Managing Licenses](../license/managing-licenses.md).
{% endhint %}

[TAKE THE SCREENSHOT OF THIS PARTICULAR SECTION AND POST HERE: Kalium -> Settings -> White Label showing the master switch and the panels below it]

***

### White Label

The master switch. Everything below it applies only while this is on, so you can set it all up first and turn it on when you're ready.

***

### Agency Details

Replaces the word "Kalium" throughout the admin with your own name.

**Agency Name**\
What appears in place of "Kalium".

**Agency URL**\
Where your name links to, your own site.

**Agency Icon**\
The icon shown beside it.

***

### Theme Details

How the theme itself is presented under **Appearance -> Themes**.

**Theme Name**\
The name shown on the theme card.

**Theme Description**\
The text underneath it.

**Theme Screenshot**\
The image on the card. Use one of the client's own site.

***

### Hide Extras

Conceals version numbers and the details that identify the theme, then gives you seven switches for individual dashboard pages:

* **Hide Plugins Page**
* **Hide Starter Sites Page**
* **Hide Template Parts**
* **Hide Status Page**
* **Hide Changelog Page**
* **Hide Account Page**
* **Hide White Label Settings**

Hide the ones a client has no business seeing, and keep the ones they'll need.

***

### Two warnings worth reading first

{% hint style="warning" %}
**Before turning on "Hide White Label Settings"**\
It hides the White Label section from the settings navigation, **including from you**.

It isn't permanent. The section is still reachable by going straight to its address:

```
/wp-admin/admin.php?page=kalium&tab=settings&section=white-label
```

**Bookmark that before you enable it.** Everything else in White Label can be undone from the section itself, but only if you can reach it.
{% endhint %}

{% hint style="warning" %}
**Hiding the Plugins page removes the only place bundled plugins can be installed and updated from.** Handle plugin updates before handing a site over, or leave that page visible.
{% endhint %}

***

### If a dashboard page is missing

Check the Hide switches here before assuming something broke. A missing **Starter Sites**, **Status**, **Changelog** or **Account** page is far more often a White Label switch than a fault.

{% content-ref url="../dashboard.md" %}
[dashboard.md](../dashboard.md)
{% endcontent-ref %}
