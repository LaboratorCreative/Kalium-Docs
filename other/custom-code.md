---
description: >-
  Where custom PHP, CSS and JavaScript belongs, and why it should never go in a
  theme file.
---

# Adding Custom Code

Sooner or later you'll be handed a piece of code (from a support reply, a plugin's documentation, a tutorial) with instructions to add it to your site. Kalium gives you several places to put it, and picking the right one takes about ten seconds once you know the options.

***

### The one rule

**Never edit the theme's files directly.**

Files in the Kalium theme folder are replaced every time the theme updates, taking your changes with them. A change made there is a change you will lose.

Everything below is a way of adding code that survives updates.

***

### Where to put what

| What you have | Where it goes |
| --- | --- |
| A few lines of CSS | **Appearance -> Customize -> Additional CSS** |
| CSS for one page only | **Parameters and Options -> Custom CSS** on that page |
| More CSS, or CSS that should only load on some pages | A **CSS Snippet** |
| PHP, the "add this to functions.php" kind | A **PHP Snippet** |
| JavaScript | A **JavaScript Snippet** |
| A tracking or verification tag from another service | **Customize -> General -> Custom JavaScript** |
| Template file changes, or a large amount of code | A **child theme** |

***

### A few lines of CSS

**Appearance -> Customize -> Additional CSS** is the quickest route. You see the result live as you type, and it's saved with your theme settings.

Best for small, site-wide visual tweaks.

{% content-ref url="custom-css.md" %}
[custom-css.md](custom-css.md)
{% endcontent-ref %}

***

### CSS for one page only

Edit the page, scroll to **Parameters and Options**, and open the **Custom CSS** tab. The styles apply to that page and nowhere else.

Don't wrap it in `<style>` tags, just the CSS.

{% content-ref url="parameters-and-options.md" %}
[parameters-and-options.md](parameters-and-options.md)
{% endcontent-ref %}

***

### PHP, JavaScript, or anything larger: use Snippets

**Snippets** are Kalium's home for custom code. A snippet lives in your database rather than a theme file, which means updates can't touch it, you can switch it off from a list, and, for PHP, **it switches itself off if it breaks**, so a bad snippet can't take your site down.

This is the answer whenever someone tells you to "add this to your functions.php file". Same result, no risk.

**Kalium -> Template Parts -> Snippets -> Add New.**

{% content-ref url="../template-parts/creating-template-parts/code-snippets/" %}
[code-snippets](../template-parts/creating-template-parts/code-snippets/)
{% endcontent-ref %}

Snippets also do things Additional CSS can't:

* **Run only on some pages**: styles for the shop, a script for the checkout
* **Load from a file**, so browsers can cache them
* **Stay organized** as named, separate pieces rather than one long box

***

### Tracking codes and verification tags

**Appearance -> Customize -> General -> Custom JavaScript** has two boxes, and they exist for the tags that other services hand you, analytics, a chat widget, a site verification meta tag.

**Header JavaScript**\
Goes inside the page's `<head>`. Most services that give you a snippet ask for it here, and anything that must load before the page renders belongs here.

**Footer JavaScript**\
Goes just before the end of the page. Better for anything that doesn't need to run immediately, because it doesn't hold up the page.

Both accept JavaScript and HTML, so you can paste a complete `<script>` tag exactly as the service gives it to you.

[TAKE THE SCREENSHOT OF THIS PARTICULAR SECTION AND POST HERE: Appearance -> Customize -> General -> Custom JavaScript showing both boxes]

{% hint style="info" %}
**Use the footer box unless the service tells you otherwise.** Scripts in the head delay your page from appearing; scripts in the footer don't.

**Shortcodes don't work in these boxes**\
They take script and markup, not shortcodes.
{% endhint %}

For your own JavaScript, as opposed to a tag someone gave you, a **JavaScript Snippet** is the better home. It can load only on the pages that need it, run from a cached file, and be switched off without editing anything.

***

### When you need a child theme

Snippets cover most needs. A child theme is worth the extra setup when:

* You need to **change a template file**, the actual HTML structure of a page
* You have **a lot** of custom code and want it in real files, in version control
* You're a developer, and you'd rather work in an editor than a browser

{% content-ref url="../getting-started/installation/child-theme.md" %}
[child-theme.md](../getting-started/installation/child-theme.md)
{% endcontent-ref %}

{% hint style="info" %}
You don't need a child theme just to add a few lines of code any more. That advice predates Snippets, and for small additions a snippet is simpler and safer.
{% endhint %}

***

### Before you paste code from the internet

**Add one piece at a time**, and check your site after each. If something breaks, you'll know exactly what caused it.

**Be careful where the code comes from.** Code from Kalium's documentation or a support reply is fine. Code from an unfamiliar forum thread deserves a closer look. It runs with full access to your site.

**Use PHP snippets rather than editing files.** Kalium checks a PHP snippet before publishing it, and disables it if it fails later. A file edit has neither safeguard.

**Keep a backup.** Theme Backups are taken before each update, but not before your own changes.

{% content-ref url="../getting-started/theme-settings/theme-backups.md" %}
[theme-backups.md](../getting-started/theme-settings/theme-backups.md)
{% endcontent-ref %}

***

### If custom code isn't doing anything

**CSS is ignored.**\
Something more specific is overriding it, normal CSS behavior. A caching plugin can also serve an old stylesheet; clear your caches.

**A PHP snippet does nothing.**\
Check it's published and not showing an **Error** status, and check its **Execution Scope**.

**A CSS or JavaScript snippet does nothing.**\
It needs a **Placement**. Set it to **Enqueue Scripts**.

{% content-ref url="../template-parts/creating-template-parts/code-snippets/troubleshooting-snippets.md" %}
[troubleshooting-snippets.md](../template-parts/creating-template-parts/code-snippets/troubleshooting-snippets.md)
{% endcontent-ref %}
