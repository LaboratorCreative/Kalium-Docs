---
description: Switch the Template Parts system on or off, and control how Snippets are stored and guarded.
---

# Template Parts Settings

**Kalium -> Settings -> Template Parts** holds three switches. The first decides whether the whole Template Parts system exists; the other two are about Snippets.

[TAKE THE SCREENSHOT OF THIS PARTICULAR SECTION AND POST HERE: Kalium -> Settings -> Template Parts showing all three settings]

***

### Template Parts

**On by default.**

This enables the system that lets you create custom sections, replace headers, footers and whole pages, build popups, and run code snippets.

Turning it **off**:

* Removes the **Kalium -> Template Parts** menu
* Stops every template part from being applied
* Stops every snippet from running
* Removes the **Content Section** element from Elementor and the block editor

**Nothing is deleted.** Your template parts stay in the database exactly as they were and come back the moment you switch it on again.

{% hint style="info" %}
If the **Kalium -> Template Parts** menu is missing from your dashboard, this setting is the first place to look. The second is **Hide Template Parts** under [White Label](white-label.md).
{% endhint %}

{% content-ref url="../../template-parts/what-are-template-parts.md" %}
[what-are-template-parts.md](../../template-parts/what-are-template-parts.md)
{% endcontent-ref %}

***

### Snippet Files

**On by default.**

With this on, each snippet is saved to a file in `wp-content/uploads/kalium-snippets/` as well as to the database. There are real benefits to this:

* **PHP snippets run from the file**, so your server caches them like any other PHP file
* **CSS and JavaScript snippets gain the Enqueue as File option**, letting browsers cache them across page views
* When something fails, WordPress points at the snippet file rather than blaming the theme

The line underneath the setting tells you **whether the folder is writable**. If it isn't, snippets run from the database instead, whatever this switch says, everything still works, you just lose the caching benefits and the **Enqueue as File** option disappears.

Snippet files stay in place while a snippet is disabled or in the trash. They're removed only when a snippet is deleted permanently.

***

### Snippets Safe Mode

**Off by default.**

This stops **every** snippet from running, without disabling any of them individually. Your snippets stay exactly as they are and start working again the moment you switch it off.

It exists for one situation: a snippet is causing a problem and you need to reach your admin to fix it. Turn Safe Mode on, sort out the snippet, turn it off.

While it's on, a yellow notice appears on the Template Parts screens so you don't forget.

{% hint style="warning" %}
**If a snippet has locked you out of your admin entirely**, you can force Safe Mode on from your site's files. Add this line to `wp-config.php`, above the line that says `/* That's all, stop editing! */`:

```php
define( 'KALIUM_SNIPPETS_SAFE_MODE', true );
```

Remove it once you're done, while it's there, the switch on this screen cannot turn snippets back on.
{% endhint %}

{% content-ref url="../../template-parts/creating-template-parts/code-snippets/troubleshooting-snippets.md" %}
[troubleshooting-snippets.md](../../template-parts/creating-template-parts/code-snippets/troubleshooting-snippets.md)
{% endcontent-ref %}
