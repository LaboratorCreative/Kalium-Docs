---
description: Broken child themes, settings that vanished, and blank pages.
---

# Child Theme Problems

{% hint style="info" %}
**You may not need a child theme at all.** If all you want is custom PHP, CSS or JavaScript, add a **Snippet** instead, it survives updates on its own and can be switched off without FTP.

A child theme is for overriding **template files**: changing the actual HTML structure of a page.
{% endhint %}

{% content-ref url="../other/custom-code.md" %}
[custom-code.md](../other/custom-code.md)
{% endcontent-ref %}

***

### The child theme shows as broken or unstyled

Usually a mismatch between the child theme and the parent theme's folder name.

**Check first:**

1. By FTP, confirm the parent folder is exactly `wp-content/themes/kalium`, not `kalium-4`, `kalium-2` or `kalium (1)`
2. Open the child theme's `style.css` and confirm its `Template:` line reads exactly `kalium`

**The fix:** rename the parent folder to `kalium`, or correct the `Template:` line to match the parent's actual folder name. Then reactivate the child theme.

{% hint style="warning" %}
Uploading a theme twice often produces a folder like `kalium-2`. If you've reinstalled recently, this is the first thing to check.
{% endhint %}

***

### My theme settings vanished when I activated the child theme

**Your settings aren't lost.** Customizer settings are stored **per theme**, so switching from parent to child starts with an empty set, the old settings still belong to the parent.

**To bring them across:**

1. Switch back to the parent theme
2. **Appearance -> Customize -> Manage Options**, and export
3. Switch to the child theme
4. Open the same screen and import the file

Your settings now belong to the child theme and survive updates.

{% content-ref url="manage-options-in-customizer.md" %}
[manage-options-in-customizer.md](manage-options-in-customizer.md)
{% endcontent-ref %}

***

### A page is blank only on the child theme

Usually an error in the child theme's `functions.php`, or a template file copied from an older version of Kalium.

**Check first:** remove any template file you've copied into the child theme, one at a time. **A parent template that changed between versions will break when an old copy shadows it**. This is the most common cause, and it appears after an update rather than when you first set the child theme up.

**Then:**

1. Rename the child theme's `functions.php` temporarily to confirm whether it's the cause
2. Reactivate the parent theme and clear caches to check the page works there
3. Reintroduce your customizations one piece at a time

***

### Keeping a child theme healthy

**Copy as few template files as possible.** Every file you copy is one you'll need to re-check after a Kalium update, because the original may have changed.

**Prefer Snippets for code.** PHP, CSS and JavaScript don't need a child theme, and a snippet is checked before it publishes and disabled automatically if it fails.

**Check after each update.** If you've copied template files, spend a minute on the affected pages after updating Kalium.

{% content-ref url="../getting-started/installation/child-theme.md" %}
[child-theme.md](../getting-started/installation/child-theme.md)
{% endcontent-ref %}
