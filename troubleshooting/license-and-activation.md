---
description: Moving to a new domain, slots in use, activation failures.
---

# License and Activation Problems

An active license is required for **theme updates**, **plugin downloads** and **starter sites**.

{% hint style="info" %}
This changed from Kalium 3, where updates were free. If you're coming from Kalium 3 and updates have stopped, an inactive license is almost certainly why.
{% endhint %}

***

### The Kalium menu has no sub-items

Not a broken installation — the sub-menu only appears once the theme is registered.

Click **Kalium** in the admin menu. With nothing to expand, it opens the activation screen. Enter your license key there.

{% content-ref url="../getting-started/installation/license-activation.md" %}
[license-activation.md](../getting-started/installation/license-activation.md)
{% endcontent-ref %}

***

### Moving a license to a different domain

Common when going from staging to production.

1. **On the old site:** **Kalium -> Status**, find the license section, and **deactivate**
2. **On the new site:** **Kalium -> Home**, and activate with the same key

**If the old site is already gone** and you can't deactivate it, the slot stays occupied. Contact support with both domains and they can release it.

{% content-ref url="../getting-started/license/activation-scope.md" %}
[activation-scope.md](../getting-started/license/activation-scope.md)
{% endcontent-ref %}

***

### All my license slots are in use

Each license covers a fixed number of sites, and staging or development copies use a slot too.

1. Review your activations in your account
2. Deactivate any site you no longer use
3. If a site no longer exists and can't be deactivated, contact support to release the slot

{% content-ref url="../getting-started/license/managing-licenses.md" %}
[managing-licenses.md](../getting-started/license/managing-licenses.md)
{% endcontent-ref %}

***

### Activation fails on a staging site

Some hosts — Flywheel, WP Engine and similar — serve staging on a domain that doesn't match your license.

Contact support with the staging domain and ask for it to be associated with your account.

***

### I never received my license key

**Check first:** the confirmation goes to the email address used at purchase, which isn't always the one you expect. Check your spam folder too.

If it's genuinely missing, contact support with the purchase date and payment reference. A typo in the registered address is a frequent cause, and support can correct it and resend.

***

### Too many redirects after updating

This is a conflict between the licensing system used by Kalium and another product using the same system.

1. Access the site by FTP
2. Rename `wp-content/plugins` to `plugins-off` to disable everything
3. Load the site — it should return
4. Rename the folder back and reactivate plugins one at a time to find the other licensed product, then update it

***

### Theme backups stopped being created

Backups are written only when the theme updates, and **only while the license is active**.

With a lapsed license the step is skipped **silently** — the setting still shows as on, the update still runs, and nothing is saved.

Renew or reactivate the license before updating. Take a manual backup in the meantime.

{% content-ref url="../getting-started/theme-settings/theme-backups.md" %}
[theme-backups.md](../getting-started/theme-settings/theme-backups.md)
{% endcontent-ref %}

***

### Things that stop working without an active license

If several unrelated things have stopped at once, check **Kalium -> Status** before investigating each one:

* **Theme updates** don't appear
* **Bundled plugins** can't install or update — "update package not available"
* **Starter sites** list is empty or won't load
* **Theme backups** are silently skipped
* **White Label** is unavailable

One inactive license explains all of them.

{% content-ref url="../getting-started/license/" %}
[license](../getting-started/license/)
{% endcontent-ref %}
