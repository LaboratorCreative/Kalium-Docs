---
description: >-
  Managing Kalium from the command line, for automated deployments and people
  who work in a terminal.
---

# WP CLI API

Kalium can be managed from the command line as well as from the WordPress admin. If you've never used a command line, **you don't need this section**, everything here can also be done from your dashboard.

It exists for two groups of people:

* **Agencies and developers** running automated deployments, staging pipelines or scripted site setups
* **Anyone managing several Kalium sites** who would rather run one command than click through the same screens repeatedly

***

### What you need

**WP-CLI installed on your server.** It's the standard command-line tool for WordPress, and most managed WordPress hosts have it already. Run this to check:

```bash
wp --version
```

If that returns a version number, you're ready. If not, your host's documentation will say whether it's available, and [wp-cli.org](https://wp-cli.org/) covers installing it yourself.

**Kalium active** on the site you're working with. The commands come from the theme, so they only exist where it's running.

***

### The command groups

Kalium adds two:

{% content-ref url="starter-sites.md" %}
[starter-sites.md](starter-sites.md)
{% endcontent-ref %}

Import, list and remove starter sites. Useful for setting up a new site in one step, or rebuilding a staging site from scratch.

{% content-ref url="license-management.md" %}
[license-management.md](license-management.md)
{% endcontent-ref %}

Activate, deactivate and check the theme license. This is the one agencies use most, activating a license as part of a deployment, or releasing it when a staging site is torn down.

***

### Finding your way around

Every command has built-in help:

```bash
wp help kalium
```

That lists everything Kalium adds. For a specific command:

```bash
wp help kalium starter-site import
```

***

### A note on safety

{% hint style="warning" %}
**Command-line changes are immediate and there's no confirmation step.** A command that imports a starter site will do so straight away.

**Take a backup before running anything that changes content**, and try commands on a staging site first.
{% endhint %}

Kalium's own theme backups are only taken when the theme updates, so they won't protect you here.

{% content-ref url="../getting-started/theme-settings/theme-backups.md" %}
[theme-backups.md](../getting-started/theme-settings/theme-backups.md)
{% endcontent-ref %}

***

### Adding custom code

If you're here because you want to extend Kalium rather than automate it, the command line isn't the route. Custom PHP, CSS and JavaScript belong in a **Snippet** or a **child theme**:

{% content-ref url="../other/custom-code.md" %}
[custom-code.md](../other/custom-code.md)
{% endcontent-ref %}

***

### If a command isn't found

**`wp: command not found`**\
WP-CLI isn't installed, or isn't on your path. Check with your host.

**`'kalium' is not a registered wp command`**\
The Kalium theme isn't active on that site, or you're running the command from outside the WordPress installation. Change to the site's root folder first.

**A command fails with a license error**\
Starter site commands need an active license, exactly as the admin screens do.

{% content-ref url="../troubleshooting/license-and-activation.md" %}
[license-and-activation.md](../troubleshooting/license-and-activation.md)
{% endcontent-ref %}
