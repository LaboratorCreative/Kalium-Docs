---
description: >-
  Build a different footer and use it on the pages you choose, while the rest of
  the site keeps the footer you set up in the Customizer.
---

# Replace the Footer

A **Footer** template part works exactly like a Header one: you build a footer as ordinary content and choose which pages use it. On those pages it **replaces** the footer you built under **Appearance -> Customize -> Footer**.

This is how you give a landing page a stripped-back footer with nothing but a copyright line, or show a different set of contact details to visitors in a particular section of the site.

***

### 1. Go to Template Parts

In your WordPress dashboard, go to **Kalium -> Template Parts**.

Switch to the **Footers** tab at the top, then click **Add New**.

[TAKE THE SCREENSHOT OF THIS PARTICULAR SECTION AND POST HERE: the Template Parts screen with the Footers tab selected]

***

### 2. Name it and build the footer

Give it a name that describes where it will be used, such as **Minimal Landing Footer**.

Build the footer in the editor using the block editor, Elementor or WPBakery. Columns of links, a newsletter form, a logo and a copyright line, anything you can lay out on a page works here.

{% hint style="info" %}
To show the current year in a copyright line without editing it every January, use the `[year]` shortcode. See [Shortcodes](../../other/shortcodes.md).
{% endhint %}

[TAKE THE SCREENSHOT OF THIS PARTICULAR SECTION AND POST HERE: the editor with a simple custom footer built]

***

### 3. Open Template Part Settings

Click the **Kalium icon** in the top-right corner to open the **Template Part Settings** panel.

***

### 4. Set the Type to Footer

Make sure **Type** is set to **Footer**. Starting from the Footers tab sets it for you.

{% content-ref url="../settings/type.md" %}
[type.md](../settings/type.md)
{% endcontent-ref %}

***

### 5. Set Display Conditions

**Without at least one condition, the footer never appears.** Click **Add Condition** and choose where it applies.

Common setups:

* **One landing page**: *Singular Content* -> *Single Page* -> choose the page
* **Every blog post**: *Singular Content* -> *Single Post*
* **The whole shop**: *WooCommerce* -> *Shop Archive*, plus a second row for *Product Page*, joined with **OR**

[TAKE THE SCREENSHOT OF THIS PARTICULAR SECTION AND POST HERE: the Display Conditions panel with a condition added]

{% content-ref url="../settings/display-conditions.md" %}
[display-conditions.md](../settings/display-conditions.md)
{% endcontent-ref %}

***

### 6. Footer Settings

Footers have two settings of their own:

**Fixed Footer**\
The footer stays in place while the page content slides up over it as visitors scroll, the footer is revealed underneath rather than pushed down. It is a striking effect on a short page and is best avoided on very long ones.

**Effect**\
The animation used as the footer is revealed: None, Fade or Slide.

[TAKE THE SCREENSHOT OF THIS PARTICULAR SECTION AND POST HERE: the Footer Settings panel showing Fixed Footer and Effect]

***

### 7. Publish

Click **Publish**, then visit a page your conditions match.

***

### Things to know

**Your Customizer footer settings stop applying on those pages.** If a footer change made in the Customizer is not showing up on some pages, check whether a Footer template part is matching them.

**The footer shows on more pages than expected** usually means conditions are joined with **OR** where **AND** was intended. **OR** widens the match; **AND** narrows it.

**Nothing appears at all**\
Check the part is Published and has at least one condition.

To go back to the Customizer footer without losing your work, set the part to **Disabled** in the Template Parts list.
