---
description: >-
  Take over an entire page — the 404 page, search results, an archive — and
  design it yourself.
---

# Replace a Page

Some pages on a WordPress site are generated for you and have no entry in **Pages** you can open and edit: the 404 page, the search results page, category and tag archives, author archives. A **Page** template part lets you design those yourself.

Unlike a Section, which adds content to a page, a Page template part **replaces the page's content completely**. What you build is what visitors see.

The most common use by far is a proper 404 page — one with your branding, a search box and a few links, instead of the plain "nothing found" message.

***

### 1. Go to Template Parts

In your WordPress dashboard, go to **Kalium -> Template Parts**.

Switch to the **Pages** tab at the top, then click **Add New**.

***

### 2. Name it and design the page

Name it after the page it replaces, such as **404 Page** or **Search Results**.

Build the content in the editor. For a 404 page, a heading, a short line of friendly text, a search form and a button back to the home page covers it.

***

### 3. Open Template Part Settings

Click the **Kalium icon** in the top-right corner to open the **Template Part Settings** panel.

***

### 4. Set the Type to Page

Make sure **Type** is set to **Page**.

{% content-ref url="../settings/type.md" %}
[type.md](../settings/type.md)
{% endcontent-ref %}

***

### 5. Choose which page it replaces

This is done with Display Conditions, and for a Page part the condition **is** the choice of page. Click **Add Condition**:

| To replace | Choose |
| --- | --- |
| The 404 page | *General Page* -> *404 Error Page* |
| Search results | *General Page* -> *Search Page* |
| The blog listing | *General Page* -> *Blog Page* |
| A category archive | *Taxonomy* -> *Category Archive* |
| A tag archive | *Taxonomy* -> *Tag Archive* |
| An author's archive | *Archive* -> *Author Archive* |
| A custom post type archive | *Archive* -> *Custom Post Type Archive* |

{% content-ref url="../settings/display-conditions.md" %}
[display-conditions.md](../settings/display-conditions.md)
{% endcontent-ref %}

***

### 6. Page Settings

Page parts have two settings:

**Show Header**\
Keep the site header above your replaced page. On by default.

**Show Footer**\
Keep the site footer below it. On by default.

Turning both off gives you a blank canvas with nothing but your content — which is exactly how a distraction-free landing page or a "coming soon" page is built.

***

### 7. Publish

Click **Publish**.

To test a 404 page, type a web address on your site that does not exist — something like `yoursite.com/this-page-is-not-real`.

***

### Things to know

**Nothing changed.** Check the part is Published, the Type is **Page**, and that a condition is set. A Page part with no conditions never applies.

**The replaced page still shows the old content underneath.** That points to the Type being **Section** rather than **Page** — a Section adds to a page, a Page replaces it.

**Two Page parts match the same page.** Only one can win. Tighten the conditions so each matches its own page.

{% hint style="info" %}
Search results have their own settings under **Appearance -> Customize -> Search Results** — the number of results, which post types to include, and the layout. If all you need is to change those, you do not need a template part. See [Search Results](../../post-types/search-results.md).
{% endhint %}
