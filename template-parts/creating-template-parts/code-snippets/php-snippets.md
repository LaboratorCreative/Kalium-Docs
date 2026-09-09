---
description: >-
  Change how your site behaves — the safe replacement for editing functions.php.
---

# PHP Snippets

A PHP snippet is what you reach for when a piece of advice starts with "add this to your functions.php file". It does the same job, in a place that survives theme updates and can be switched off if it misbehaves.

Writing PHP snippets requires an **administrator** account.

***

### Where a PHP snippet runs

This is the setting that decides everything, and it is worth understanding before you write anything.

#### With no Placement — the usual choice

Leave **Placement** empty and your snippet runs as the theme loads, before the page is built. This is the right moment for code that **registers** something:

* Adding hooks and filters
* Registering a shortcode
* Changing a WooCommerce or WordPress setting
* Adding an image size or a menu location

Most code you'll be given belongs here. **If you're unsure, leave Placement empty.**

#### With a Placement — for code that outputs something

Give the snippet a placement and the code runs at that exact spot on the page, each time it's reached. Use it when the snippet needs to *print* something in a particular place — a notice above the checkout button, a line of text after every blog post.

{% content-ref url="../../settings/placement.md" %}
[placement.md](../../settings/placement.md)
{% endcontent-ref %}

{% hint style="warning" %}
Some locations fire very early, while the theme is still loading. A snippet placed on one of those will never run. If a placed snippet does nothing at all, try removing the placement.
{% endhint %}

***

### Execution Scope

**Execution Scope** sits just under **Snippet Type**. It appears for PHP snippets that have no placement — with a placement, the location already says where the code runs, so the setting isn't needed.

**Frontend**\
The snippet runs on your public site only, not in the WordPress admin. This is the default and the right choice for anything that changes what visitors see.

**Admin**\
The snippet runs in the WordPress admin only. Use this for code that adds a column to a list screen or changes something in the dashboard.

**Everywhere**\
The snippet runs in both.

{% hint style="info" %}
Requests that are neither a normal page view nor the admin — REST API calls, scheduled tasks, anything run from the command line — count as **Frontend**.
{% endhint %}

***

### Run Once

Under **Snippet Settings** you'll find **Run Once**, which reveals **Run Once Mode**:

**Once per page load**\
However many placements fire on a page, the code runs at most once. Use this when a snippet is placed in more than one spot and the code should not repeat.

**Once, then disable**\
The code runs a single time and the snippet switches itself to Disabled. This is for one-off jobs — a bulk update to some posts, a one-time cleanup. Enable it again to run it once more.

***

### Publishing is checked for you

PHP is the one language where a mistake can take a site offline, so Kalium checks before letting that happen.

**When you save**, the code is checked for syntax errors. If there's one, the save is refused, the message names the line, and your work stays in the editor.

**When you publish** — or update the code of a published snippet, or enable one from the list — Kalium runs a **safe activation**: it loads a page of your site in the background with the new code active. If the page loads, the snippet goes live. If it doesn't, **the snippet stays switched off** and you're shown the error with its line number.

{% hint style="info" %}
Some servers block a site from making requests to itself. If yours does, the check can't run — the snippet is enabled anyway and a notice tells you the check was skipped. Test your site yourself after publishing in that case.
{% endhint %}

***

### If a snippet fails later

Code that publishes cleanly can still fail later, when it meets a page or a situation you didn't test.

When that happens, **Kalium switches the snippet to Disabled on the spot**, the page carries on loading, and the list shows an **Error** status. Hover it for the message and the line. A notice also appears in your admin.

Your site stays up. That's the whole design.

{% content-ref url="troubleshooting-snippets.md" %}
[troubleshooting-snippets.md](troubleshooting-snippets.md)
{% endcontent-ref %}

***

### A worked example

Say you want to change the "Add to cart" text on your shop to "Buy now".

1. **Kalium -> Template Parts -> Snippets -> Add New**
2. Name it **Change add to cart button text**
3. Set **Snippet Type** to **PHP**
4. Paste the code — no `<?php`, it's already there:

```php
add_filter( 'woocommerce_product_single_add_to_cart_text', function () {
	return 'Buy now';
} );
```

5. Leave **Placement** empty — this registers a filter, so it belongs early
6. Leave **Execution Scope** on **Frontend**
7. **Publish**

Open a product page and the button reads "Buy now".

If you later want the old text back, set the snippet to **Disabled** in the list. Nothing else to undo.

***

### Common questions

**My snippet does nothing.**\
Check it's Published and not showing **Error**. Then check **Execution Scope** — a *Frontend* snippet never runs in the admin, and an *Admin* one never runs on your site.

**It runs twice.**\
Two placements are firing on the same page. Turn on **Run Once**.

**I can't choose PHP.**\
PHP and JavaScript need an administrator account.

**Publishing is refused.**\
Either a syntax error on the line named in the message, or safe activation found your site doesn't load with the code. The message tells you which.

**The code was supposed to add a post type and didn't.**\
An unplaced snippet with Execute Conditions waits until the page is known before running, which is too late to register a post type. Remove the conditions.
