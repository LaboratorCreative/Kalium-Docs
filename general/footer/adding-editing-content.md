---
description: The two layers of a footer, structure in the builder and content in widgets.
---

# Adding/Editing Content

Your footer is built in two layers, and knowing which one you need saves a lot of clicking.

**The Footer Builder**, at **Appearance -> Customize -> Footer**, defines the footer's **structure**: how many rows there are, how they're divided into columns, and which widget area goes where.

**Widgets**, at **Appearance -> Widgets**, fill that structure with **content**: your text, links, images and forms.

Set the structure up once in the builder, then edit the content in Widgets whenever you like without going back to the Customizer.

***

## The Footer Builder

Open **Appearance -> Customize -> Footer** and click **Footer Content**.

Unlike the header, the footer has no fixed regions. **You add rows yourself** with **Add Footer Row**, and build each one up from columns and elements.

<figure><img src="../../.gitbook/assets/adding-footer.jpg" alt=""><figcaption></figcaption></figure>

### Building a footer

#### 1. Add a row

Click **Add Footer Row**. Each row is a horizontal band across the footer. Most footers have two: a wide one for the columns of links, and a narrow one underneath for the copyright line.

#### 2. Add columns to the row

Inside a row, add **Column** elements. Each column has a **Width** setting with 18 options, **set per device**, so four columns on a desktop can become two on a tablet and one on a phone.

#### 3. Put a Widget Area in each column

A column holds **Widget Area** elements and nothing else. There are six, **Widget Area 1** to **Widget Area 6**, one per footer widget area, and each can be used once. Each is already bound to its own widget area, so it has no sidebar chooser, just a **Widgets Per Row** setting for splitting its widgets into columns.

That binding is the point: once a Widget Area is placed, everything inside it is edited from the Widgets screen rather than from the Customizer.

#### 4. Publish

The preview updates as you work, but nothing saves until you click **Publish**.

***

### Row settings

Click a row to open its settings:

**Horizontal Gap** and **Vertical Gap** set the space between columns, per device.

**Full Width**\
The row runs edge to edge instead of sitting inside the content container.

**Text**, **Headings** and **Links** set color overrides for that row, with **Links** having separate normal and hover colors. This is handy for making a bottom copyright row quieter than the row above it.

**Background** gives the row its own background: a color, or an image with position, repeat and size controls.

{% hint style="info" %}
To set a background behind the whole footer rather than one row, use **Appearance -> Customize -> Styling -> Colors -> Footer**.
{% endhint %}

***

### The copyright line

Kalium's default footer puts two shortcodes into widgets, one in **Widget Area 1** and one in **Widget Area 2**:

```
[kalium_site_info]
[kalium_social_icons]
```

So you change the wording, including **removing the theme credit**, from **Appearance -> Widgets** rather than from the footer builder:

```
[kalium_site_info display="{copyright} {year} {site_title}. All rights reserved."]
```

The year updates itself, so you never have to edit it again.

{% content-ref url="../../other/shortcodes.md" %}
[shortcodes.md](../../other/shortcodes.md)
{% endcontent-ref %}

***

## Widgets

The footer content can be edited in two places:

1. **Appearance -> Widgets**
2. **Appearance -> Customize -> Widgets**

If you need guidance on adding widgets, [this article](../sidebars/troubleshooting-sidebar.md#adding-widgets-to-your-sidebar) provides a detailed explanation.

Once you’ve defined the footer structure and assigned widget areas, you can easily make edits directly in **Widgets** page without needing to go to the **Customizer** to save changes.

### Footer Widget Areas

Widgets locations that you can use in the footer are **Footer Widget Area 1** to **Footer Widget Area 6**:

<figure><img src="../../.gitbook/assets/Footer Widgets Sidebars.jpg" alt=""><figcaption><p>Footer Widget Areas that can be used in the footer</p></figcaption></figure>

The content formatting and everything Block Editor offers can be constructed here.

With this approach, you can add any type of element to the footer, including images, maps, contact forms, and other content supported by the _Block Editor_ and the plugins that extend it.

{% hint style="info" %}
When editing multiple widget locations, make sure to click the **Update** button after each widget location edit. WordPress only saves changes for the current widget area, so if you edit multiple areas without saving, your work may be lost.
{% endhint %}

### Multi-Column Widget Area

The widget content flows vertically by default, but you can still organize it into columns for a more structured layout.

You can add as many groups as needed in the widget area, and in the Customizer’s **Footer** section, you can configure these widgets to split into columns.

This setup supports varying column numbers on different responsive viewports.​

<figure><img src="../../.gitbook/assets/Footer Widget Multi Column.jpg" alt=""><figcaption><p>Footer Widget Area 3 example</p></figcaption></figure>

Then in the **Appearance -> Customize -> Footer** section, set the number of **Widgets per Row** for **Footer Widget Area 3**:

<figure><img src="../../.gitbook/assets/Footer Widget Multi Column Customizer.jpg" alt=""><figcaption><p>Splited widget columns</p></figcaption></figure>

Do not confuse the _**Column**_ element with _widget columns_, as it is mainly used for structuring the footer layout.

***

### Turning the footer off

**Appearance -> Customize -> Footer -> Enable Footer** removes the footer from the whole site. Everything else on the screen disappears while it's off, which is worth knowing if the Footer Content builder seems to have vanished.

To hide the footer on **one** page instead, use that page's **Parameters and Options -> Page Options -> Footer Visibility**.

{% content-ref url="../../other/parameters-and-options.md" %}
[parameters-and-options.md](../../other/parameters-and-options.md)
{% endcontent-ref %}

***

### Common questions

**My footer is empty.**\
The structure exists but the widget areas have nothing in them. Go to **Appearance -> Widgets** and fill them.

**My footer doesn't appear at all.**\
Check **Enable Footer** is on. Then check whether a Footer template part is replacing it on those pages.

**My footer content shows on some pages but not others.**\
A Footer template part is matching those pages and replacing the Customizer footer.

**A row's background color isn't applying.**\
Check whether **Styling -> Colors -> Footer** is setting a background behind the whole footer. A row background sits on top of it, so a solid footer color can hide a subtle row color.

{% content-ref url="../../template-parts/creating-template-parts/replace-the-footer.md" %}
[replace-the-footer.md](../../template-parts/creating-template-parts/replace-the-footer.md)
{% endcontent-ref %}
