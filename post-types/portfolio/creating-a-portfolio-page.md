# Creating a Portfolio Page

The Portfolio Page, also known as the _portfolio archive_, displays all your portfolio items in one place. By default, the portfolio page is located at this URL `yoursite.com/portfolio` unless you [modify it](creating-a-portfolio-page.md#permalinks-structure).

There are several methods to create and set up a **Portfolio Page**:

1. [**Default Post Type Archive Page**](creating-a-portfolio-page.md#default-post-type-archive-page): Automatically generated by WordPress for the "Portfolio" post type. It displays all portfolio items using the default archive layout.
2. [**Page Template "Portfolio Page"**](creating-a-portfolio-page.md#page-template-portfolio-page): Choose this template when creating a new page to set up a custom-designed Portfolio Archive page with layout options specific to the Kalium theme.
3. [**Elementor Widget**](creating-a-portfolio-page.md#elementor-widget): Use the Elementor Page Builder to add a Portfolio widget to any page, providing advanced design and layout options.
4. [**WPBakery Widget**](creating-a-portfolio-page.md#wpbakery-widget): For users of WPBakery Page Builder, add the Portfolio widget to your page for a customizable and visually appealing portfolio display.

In this guide, we will cover each method of creating the Portfolio Page and demonstrate how to use them effectively to showcase your portfolio items.

## Default Post Type Archive Page

The default post type archive page is automatically generated by WordPress for the **Portfolio** post type.&#x20;

It provides a standard archive layout to display all portfolio items. For additional customization options, refer to the [**Portfolio Page**](portfolio-page.md) article where you can learn how to define and adjust the appearance of your portfolio page according to your preferences.

This method is straightforward and requires no extra configuration, making it an easy option for a basic portfolio display.

### Permalinks Structure

The permalinks structure for the **Portfolio** post type is located in **Settings -> Permalinks**:

<figure><img src="../../.gitbook/assets/Creating a Portfolio - Permalinks.jpg" alt=""><figcaption></figcaption></figure>

Every single portfolio item (project) includes the **Portfolio base** prefix in its permalink, e.g., `yoursite.com/portfolio/project-url`. To remove this prefix, simply leave the field empty.

{% hint style="info" %}
There is a caveat to removing the portfolio prefix: without it, the default portfolio archive will no longer be available. Instead, you will need to create the archive using the methods described on this page.
{% endhint %}

## Page Template "Portfolio Page"

Using the Page Template **Portfolio Page** allows you to create a custom _portfolio archive_ page with specific layout options provided by the Kalium theme.&#x20;

When you select the **Portfolio Page** template for a new page, it inherits all the initial design settings and options defined in the Portfolio Page section of the Customizer.&#x20;

You can then set various additional settings to customize the output of your portfolio page, allowing for greater flexibility and control over the presentation of your portfolio page.

### Create a New Page

Go to your WordPress dashboard and under **Pages** from the left-hand menu, and click **Add New** **Page** to create a new page.

<figure><img src="../../.gitbook/assets/Creating a Portfolio Page - Page Template.jpg" alt=""><figcaption></figcaption></figure>

After selecting Portfolio Page template, click on **Parameters and Options -> Portfolio Settings** to override the options that you need:

<figure><img src="../../.gitbook/assets/Creating a Portfolio - Page Template Option 1.jpg" alt=""><figcaption></figcaption></figure>

* **Show Title & Description:** This option allows you to hide or show the portfolio title and description that is [defined here](portfolio-page.md#title-and-description). You can choose to disable this feature if you have custom content that you want to display above the portfolio.
* **Custom Query:** This option provides a query builder that allows you to select specific items to appear on that page only. It enables you to customize the content displayed on the portfolio page according to your preferences.
* **Masonry Style Portfolio:** Create a custom pattern for displaying portfolio images. It allows you to design a creative layout with various image formats that will align neatly based on the Masonry layout style. This section is covered **here**.
* **Default Filter Category:** Set a default filter category that will be applied automatically when users visit the portfolio page.

### Grid Settings

Various grid settings are available for the Portfolio Page template in **Grid Settings** tab, allowing you to customize how portfolio items are displayed. These settings include:

<figure><img src="../../.gitbook/assets/Creating a Portfolio - Page Template Options 2.jpg" alt=""><figcaption></figcaption></figure>

* **Columns Count**: Set the number of items per row.&#x20;
* **Reveal Effect**: Control the animation effect applied to portfolio items as they enter the viewport. [Learn more about reveal effect ->](portfolio-page.md#reveal-effect)
* **Full Width Container**: Enabling this option makes the portfolio container span the full width of the viewport. [Learn more about full width container ->](portfolio-page.md#full-width-container)
* **Title and Filter Container**: Visible when the Full Width Container is set to **Yes**. This option extends the portfolio items to align with the container’s edges, creating a more immersive layout.

### Layout Type

Alternatively, you can use either of the two available [Portfolio Page](portfolio-page.md) card layouts in the **Layout Type** tab. Select the layout type you want to apply for portfolio items in this page only. By default, it inherits the layout type set in the Customizer.

<div><figure><img src="../../.gitbook/assets/Creating a Portfolio - Page Template Layout Type 1.jpg" alt=""><figcaption><p>Layout Type 1</p></figcaption></figure> <figure><img src="../../.gitbook/assets/Creating a Portfolio - Page Template Layout Type 2.jpg" alt=""><figcaption><p>Layout Type 2</p></figcaption></figure></div>

### Custom Query

This option alters the output of portfolio items displayed on the page. It allows you to define a specific set of items to show, independent of the default filters. The filters on the page will then adjust based on the items included in the custom query.

<figure><img src="../../.gitbook/assets/Creating a Portfolio - Page Template - Custom Query.jpg" alt=""><figcaption></figcaption></figure>

* **Portfolio Items**: List individual portfolio items to display.
* **Select From Category**: Choose portfolio categories to include items from.
* **Select From Tags**: Choose portfolio tags to filter items by.
* **Order By**: Define the criteria for sorting portfolio items (e.g., date, title).
* **Order**: Specify the sorting direction (ascending or descending).
* **Items per Page**: Set the number of portfolio items to display per page.

## Elementor Widget

If you want to enhance your portfolio presentation beyond the default layout, Elementor’s powerful page builder offers a versatile solution. Elementor’s intuitive interface and extensive customization options enable you to create a visually appealing and highly functional portfolio page that aligns with your vision.

### Create a New Page

Go to your WordPress dashboard and under **Pages** from the left-hand menu, and click **Add New** **Page** to create a new page.

### Set Up the Page

1. Enter a title for your portfolio page (e.g., "Portfolio" or "Our Projects").
2. Click the **Edit with Elementor** button to start customizing your page with Elementor.

<figure><img src="../../.gitbook/assets/Creating a Portfolio - Elementor Page.jpg" alt=""><figcaption></figcaption></figure>

### Add the Portfolio Items Widget

From the left widget area of Elementor, under the **Kalium** section, drag or click the **Portfolio Items** widget onto your page (right area).

<figure><img src="../../.gitbook/assets/Creating a Portfolio - Elementor Widget.jpg" alt=""><figcaption></figcaption></figure>

### Configure the Portfolio Items Widget

Under the **Content** tab, adjust the basic options to fit your needs. These settings will override the default [Portfolio Page](portfolio-page.md) options.

<figure><img src="../../.gitbook/assets/Creating a Portfolio - Elementor - Portfolio Items - Content.jpg" alt=""><figcaption></figcaption></figure>

Switch to the Layout tab in the widget settings. You can choose to inherit layout settings from the Customizer or configure new layout options directly in Elementor.

<figure><img src="../../.gitbook/assets/Creating a Portfolio - Elementor - Portfolio Items - Layout.jpg" alt=""><figcaption></figcaption></figure>

### Publish Your Page <a href="#publish-your-page" id="publish-your-page"></a>

Once you're satisfied with the setup, click the **Publish** button in the top right corner to make your blog page live.

## WPBakery Widget

WPBakery Page Builder enables you to create a portfolio page with a personalized touch. Instead of using the default WordPress portfolio archive, WPBakery lets you build a portfolio page from scratch, offering extensive customization to achieve your desired look and layout.

### Create a New Page

Go to your WordPress dashboard, select **Pages** from the left-hand menu, and click **Add New Page** to create a new page.

### Set Up the Page

Enter a title for your portfolio page (e.g., "Portfolio" or "Our Work").

Click the **WPBakery** button to start customizing your page with the WPBakery Page Builder.

<figure><img src="../../.gitbook/assets/Creating a Portfolio - WPBakery - Create Page.jpg" alt=""><figcaption></figcaption></figure>

### Choose Editor

Choose between **Backend** or **Frontend** editor. For this example, we'll use the Backend editor.

<figure><img src="../../.gitbook/assets/Creating a Portfolio - WPBakery - Choose Editor.jpg" alt=""><figcaption></figcaption></figure>

### Select Layout

Choose the **Default Layout** for your portfolio page.

<figure><img src="../../.gitbook/assets/Creating a Portfolio - WPBakery - Select Layout.jpg" alt=""><figcaption></figcaption></figure>

### Add Portfolio Widget

Click the **+ Add Element** button.

In the popup that appears:

1. Switch to the **Laborator** tab and select **Portfolio**.
2. Alternatively, use the search bar to find the element directly.

<figure><img src="../../.gitbook/assets/Creating a Portfolio - WPBakery - Add Element.jpg" alt=""><figcaption></figcaption></figure>

### Customize the Portfolio Widget

Set the options in the **Portfolio** widget to overwrite the layout and style of the **Portfolio Page** under the Customizer. Click **Save Changes** to apply your settings.

<figure><img src="../../.gitbook/assets/Creating a Portfolio - WPBakery - Edit Settings.jpg" alt=""><figcaption></figcaption></figure>

<div><figure><img src="../../.gitbook/assets/Creating a Portfolio - WPBakery - Settings 2.jpg" alt="" width="375"><figcaption></figcaption></figure> <figure><img src="../../.gitbook/assets/Creating a Portfolio - WPBakery - Settings 3.jpg" alt="" width="375"><figcaption></figcaption></figure></div>

### Publish Your Page

When you're done customizing the portfolio page, click the **Publish** button on the right side to make your portfolio page live.
