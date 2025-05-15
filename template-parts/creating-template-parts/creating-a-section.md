# Creating a Section

Sections let you insert custom content into specific parts of your site — like above the header, below the content, or inside WooCommerce product pages. These are placed using WordPress and plugin hook locations, and you can decide exactly when and where they appear using display conditions.

In this example, we’ll create a banner that displays after the header across the entire site.

***

### 1. Go to Template Parts

In your WordPress dashboard, go to **Kalium → Template Parts**.

Switch to the **Sections** tab at the top, then click **Add New** in the top-left corner.

***

### 2. Create the Section

Enter a name for your section. For example: **30% Off Summer Sale Banner**

Now add your content in the editor. This can be anything — a short message, a call-to-action, a promotional banner, or even a more complex layout with images and buttons.

In this example, we’ll use the default WordPress editor (Gutenberg) to build the section. If you prefer using **Elementor** or **WPBakery**, please check the respective articles:

{% content-ref url="broken-reference" %}
[Broken link](broken-reference)
{% endcontent-ref %}

* Create a Section with Elementor
* Create a Section with WPBakery

***

### 3. Open Template Part Settings

Click the **Kalium icon** in the top-right corner to open the **Template Part Settings** panel.

***

### 4. Set the Type

Make sure the **Type** is set to **Section**.\
If it's not, switch it manually — otherwise the section may not behave as expected.

***

### 5. Set Display Conditions

Click **Add Condition** to choose where this section should appear.

For this example, we want the banner to show across the entire site:

* Set **General Page** → **Is** → **Entire Site**

You can always add more than one condition and combine them using **AND** or **OR** logic to create more specific rules.

> For a complete overview of all condition types and how to use them, see this article.

***

### 6. Choose Placement

This setting is available only for **Sections**.

Click **Add New Location** to choose where the section appears on the page.

You can:

* Select from a list of predefined hook locations
* Search within the list
* Or click the **target icon** to open a visual popup where you can select the exact area

For this example, choose **Header After**.

Leave the **Priority** set to `10`. Lower numbers appear earlier when multiple sections target the same location.

> 🔎 Learn more about placement options

***

### 7. Container and Visibility Options

Under **Container Settings**, you can fine-tune how your section is wrapped and displayed:

* **Wrap with Container** – This is enabled by default. Turn it off if you want your content to stretch full-width or appear without wrapper elements.
* **Visibility** – Choose whether the section appears on desktop, tablet, mobile — or all.
* **Container Classes** – You can enter a class like `container` if you want the content to follow your site’s layout width. For this example, leave it blank.
* **Tag Name** – You can optionally set a semantic HTML tag like `<aside>` or `<section>`. By default, this is set to `<div>`, so you can leave it empty.

***

### 8. Publish

Once everything is configured, click **Publish**.

Your section will now appear after the header on every page of your site, based on the conditions and placement you selected.

***

### 9. Optional: Insert Manually with Gutenberg

In addition to automatic placement, Kalium also provides a **Template Part Block** for Gutenberg. You can use this block to manually insert any section into a specific page or post — regardless of the display conditions.

To do this:

* Edit the page or post in Gutenberg
* Add the **Template Part** block
* Select the section you created from the dropdown

This is useful when you want full manual control over placement within individual pages.
