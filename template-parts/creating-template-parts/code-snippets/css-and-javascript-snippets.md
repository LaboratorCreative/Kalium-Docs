---
description: Add styles and scripts to your site, with control over how they load.
---

# CSS and JavaScript Snippets

CSS snippets change how your site looks. JavaScript snippets add behavior in the browser. Both work the same way and share most of their settings, so they're covered together here.

Anyone who can edit Template Parts can write **CSS** snippets. **JavaScript** requires an administrator account.

***

### The one rule that catches everyone

**A CSS or JavaScript snippet with no Placement does not run at all.**

This is the opposite of PHP, where an empty placement is normal and usually correct. Styles and scripts have to be attached to the page, and the placement is what attaches them.

Kalium handles this for you: **a new CSS or JavaScript snippet is given the Enqueue Scripts placement automatically**. Leave it alone and everything works. But if you clear the placement, or you're editing an older snippet, this is the first thing to check when nothing happens.

{% hint style="info" %}
**Enqueue Scripts** is in the **Head** group of the location selector. It's the standard spot where WordPress loads styles and scripts, and it is almost always the right one.
{% endhint %}

***

### CSS vs. Additional CSS

Kalium already has a box for custom CSS at **Appearance -> Customize -> Additional CSS**. So when should you use a snippet instead?

**Use Additional CSS** for a handful of quick tweaks. It's fewer clicks and it previews live in the Customizer.

**Use a CSS snippet** when you want:

* **Conditions** — styles that only load on the shop, or only for logged-in visitors
* **Organization** — several named snippets instead of one long unbroken box
* **A separate file** — better for browser caching on a large stylesheet
* **Media targeting** — styles only for print, or only below a screen width

Neither is more "correct". For three lines, use Additional CSS.

{% content-ref url="../../../other/custom-css.md" %}
[custom-css.md](../../../other/custom-css.md)
{% endcontent-ref %}

***

### Settings for CSS snippets

Under **Snippet Settings**:

**Enqueue as File**\
Loads your styles from their own file rather than printing them into the page. The browser can then cache the file across page views, which is worth doing for anything longer than a few lines. This option appears only while **Snippet Files** is enabled in **Kalium -> Settings -> Template Parts**.

**Media**\
Limits the styles to a particular context, using the same values as a stylesheet's media attribute. Leave it empty to apply everywhere. Useful values:

| Value | Applies to |
| --- | --- |
| `print` | Only when the page is printed |
| `(max-width: 768px)` | Only on screens narrower than 768px |
| `(min-width: 1200px)` | Only on wide screens |
| `screen` | Screens but not print |

***

### Settings for JavaScript snippets

**Enqueue as File**\
As above — loads the script from its own file instead of printing it inline. The two settings below only exist once this is on.

**ES Module**\
Lets your code use modern `import` and `export` syntax. Turn this on only if the code you're adding needs it; most snippets don't.

**Loading**\
How the browser should handle the script:

* **Blocking** — the page waits for the script before continuing. Only for code that must run before anything renders.
* **Async** — the script loads alongside the page and runs as soon as it's ready. Order is not guaranteed.
* **Defer** — the script loads alongside the page and runs after it's built. **This is the safest default** for most scripts.

Turning on **ES Module** switches *Blocking* to *Defer* automatically, because a module cannot block.

**Dependencies**\
Script handles that must load before yours, separated by commas. The one you'll actually use is `jquery` — if your code starts with `jQuery(` or `$(`, put `jquery` here.

***

### Loading styles only where you need them

The real advantage of a snippet over Additional CSS is that it doesn't have to load everywhere.

Say you have a long stylesheet that only applies to your shop. Add **Execute Conditions**:

* *WooCommerce* -> *Shop Archive*, joined with **OR**
* *WooCommerce* -> *Product Page*

Now those styles load on shop pages and nowhere else — every other page on your site stays that bit lighter.

{% content-ref url="../../settings/display-conditions.md" %}
[display-conditions.md](../../settings/display-conditions.md)
{% endcontent-ref %}

***

### A worked example

Hiding the page title on a specific page:

1. **Kalium -> Template Parts -> Snippets -> Add New**
2. Name it **Hide title on the contact page**
3. Set **Snippet Type** to **CSS**
4. Add the code:

```css
.page-title {
	display: none;
}
```

5. Leave **Placement** as **Enqueue Scripts** — it's already set
6. Add an **Execute Condition**: *Singular Content* -> *Single Page* -> Contact
7. **Publish**

The title is hidden on that page and nowhere else.

***

### Common questions

**My CSS snippet does nothing.**\
Check **Placement**. Empty means it never loads — set it to **Enqueue Scripts**.

**My styles load but are ignored.**\
Something more specific is overriding them. This is normal CSS behavior rather than a snippet problem — a more specific selector wins.

**My JavaScript throws an error about `$`.**\
Add `jquery` to **Dependencies**, or write `jQuery` in full instead of `$`.

**The script runs before the page is ready.**\
Set **Loading** to **Defer**.

**I can't choose JavaScript.**\
JavaScript and PHP require an administrator account. CSS is available to anyone who can edit Template Parts.

**I don't see Enqueue as File.**\
**Snippet Files** is switched off, or the snippets folder isn't writable. Check **Kalium -> Settings -> Template Parts** — the line under the setting says which.
