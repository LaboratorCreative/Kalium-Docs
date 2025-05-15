# Adding a Section

Sections let you insert custom content into specific parts of your site — like above the header, below the content, or inside WooCommerce product pages. These are placed using WordPress and plugin hook locations, and you can decide exactly when and where they appear using display conditions.

In this example, we’ll create a banner that displays after the header across the entire site.

***

### 1: Go to Template Parts

In your WordPress dashboard, go to **Kalium → Template Parts**.

Switch to the **Sections** tab at the top, then click **Add New** in the top-left corner.

***

### 2: Create the Section

Enter a name for your section. For example:\
`30% Off Summer Sale Banner`

Add your content in the editor — this can be anything from a notice to a promotional banner.

***

### 3: Open Template Part Settings

Click the **Kalium icon** in the top-right corner to open the **Template Part Settings** panel.

***

### 4: Set the Type

Make sure the **Type** is set to **Section**.\
If it's not, switch it manually — otherwise the section may not behave as expected.

***

### 5: Set Display Conditions

Click **Add Condition** to choose where this section should appear.

To display the banner across the entire site:

* Set **General Page** → **Is** → **Entire Site**

You can add more conditions using **AND** or **OR** logic. This allows you to create powerful conditional rules, such as:

* Show only on product pages **AND** only for logged-in users
* Show on the blog page **OR** all category archives

> ⚙️ For more complex combinations, see Advanced Display Conditions _(link to separate article)_.

***

### 6: Choose Placement

This setting is available only for **Sections**.

Click **Add New Location** to choose where the section appears on the page.

You can:

* Select from a list of predefined hook locations
* Search within the list
* Or click the **target icon** to open a visual popup where you can select the exact area

For this example, choose **Header After**.

Leave the **Priority** set to `10`. Lower numbers are placed earlier if multiple sections appear in the same location.

> 🔎 Learn more about placement options

***

### 7: Container and Visibility Options

Under **Container Settings**, you can fine-tune how your section is wrapped and displayed:

* **Wrap with Container** – This is enabled by default. Turn it off if you want your content to stretch full-width or appear without wrapper elements.
* **Visibility** – Choose whether the section appears on desktop, tablet, mobile — or all.
* **Container Classes** – You can enter a class like `container` if you want the content to follow your site’s layout width. For this example, leave it blank.
* **Tag Name** – You can optionally set a semantic HTML tag like `<aside>` or `<section>`. By default, this is set to `<div>`, so you can leave it empty.

***

### 8: Publish

Once everything is configured, click **Publish**.

Your section will now appear after the header on every page of your site, just as set by your conditions and placement.
