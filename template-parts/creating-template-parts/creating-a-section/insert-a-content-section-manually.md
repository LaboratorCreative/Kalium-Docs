# Insert a Content Section Manually

While Template Parts are usually placed using display conditions and hook locations, Kalium also gives you full control to manually insert them inside any page or post — if you're using **Sections**.

This is especially useful when you want to show a section in a very specific spot, without relying on automatic placement rules.

Manual insertion is only supported for **Sections**, as they are designed to be embedded within content. Other Template Part types — like **Headers**, **Footers**, and **Pages** — are meant to replace entire sections of your site and cannot be inserted manually.

Kalium includes dedicated options for **Gutenberg**, **Elementor**, and **WPBakery**, as well as a shortcode that can be used anywhere shortcodes are supported.

Below, we’ll explain how to insert sections manually using each method.

***

### Gutenberg

For users working in the native WordPress editor, Kalium provides a **Content Section** **block** that lets you manually insert a section into any page or post.

To insert a section manually in Gutenberg:

1. Edit your page or post in the Gutenberg editor.
2. Click the **“+” icon** to add a block.
3. Search for **Content Section** and select the block.
4. In the block settings, choose the section you want to display from the dropdown.

This is useful when you want to insert the section exactly where you want — independent of display conditions or placement settings.

***

### Shortcode Option

If you prefer, you can insert any Template Part Section using a shortcode.

**Shortcode format:**

```
[kalium_section id=“123”]
```

You don’t need to look up the ID manually — the shortcode is already visible next to each Template Part in the **Template Parts** dashboard. Just copy and paste it wherever you need.

This is useful if you're placing the section inside:

* Widgets
* Custom HTML areas
* Third-party shortcode-compatible plugins
