# Creating a Portfolio Item

Now that your [Portfolio page](../creating-a-portfolio-page.md) is set up, it's time to dive into creating captivating projects. Whether you're showcasing your latest work, highlighting case studies, or presenting your creative portfolio, Kalium makes it easy to publish and manage your portfolio items.

## Adding new Item

To get started, let's create the portfolio item. Navigate to the WordPress sidebar, go to **Portfolio** -> **Add New Item**.

<figure><img src="../../../.gitbook/assets/Creating a Portfolio Item - New Item.jpg" alt=""><figcaption></figcaption></figure>

1. **Enter the Title**: This is the name that will be displayed for your portfolio item.
2. **Insert Main Content**: Add the primary content for your project. This can include text, images, videos, and other media to showcase your work.
3. **Select Item Type**: Choose the specific type of portfolio item you are creating (e.g., Side Portfolio, Columned, Carousel). This defines how the content will be displayed.
4. **Set a Featured Image**: Upload a featured image that will represent your portfolio item across your site. This image is crucial as it will appear in portfolio listings and other sections of your site.
5. **Select Categories** (optional): Assign your portfolio item to one or more categories to help organize and filter your projects. This is optional but useful for filtering the items.
6. **Select Tags** (optional): Add relevant tags to your portfolio item to enhance searchability and filter options. Tags are also optional but can be helpful for filtering the items.
7. **Click Publish**: Once you’ve completed all the necessary fields, click **Publish** to make your portfolio item live on your website.

The **Project Settings** tabs contain all the settings for configuring your portfolio item. These settings may vary depending on the portfolio type you choose, as each type has its own set of unique options. However, there are also common options that are shared across all portfolio types.

{% hint style="info" %}
Creating a portfolio item involves the use of custom fields, which are managed through the **Advanced Custom Fields Pro** plugin. This plugin is essential for customizing and displaying the content of your portfolio items.
{% endhint %}

## Common Settings

In this section, we will explain the common settings that are relevant to every portfolio item, no matter which **Project Layout** you choose.

### Item Details

Here, you can provide general information about the portfolio item.

<figure><img src="../../../.gitbook/assets/Creating a Portfolio Item - Item Details.jpg" alt=""><figcaption></figcaption></figure>

* **Subtitle:** A brief, one-line title to describe the item (optional).

### Prev-Next Navigation

Here, you can replace the default links for navigating to the previous or next item in the list, allowing for custom navigation order.

<figure><img src="../../../.gitbook/assets/Creating a Portfolio Item - Prev Next Navigation.jpg" alt=""><figcaption></figcaption></figure>

* **Custom Prev-Next Links**: Allows you to override the default previous and next navigation links for this item.
* **Previous Item:** Set the previous item by typing its title from your existing portfolio items.
* **Next Item:** Set the next item by typing its title from your existing portfolio items.
* **Custom Archive URL:** Replaces the default link between the prev and next links, which typically directs users to the portfolio archive page defined in the [Project Page](../project-page.md#navigation) settings.

### Project Link

Allows you to set a **showcase** link that appears alongside the portfolio content or specify a custom redirect URL, directing users to a different page when they access this item’s single page.

<figure><img src="../../../.gitbook/assets/Creating a Portfolio Item - Project Link.jpg" alt=""><figcaption></figcaption></figure>

* **Launch Link Title:** The text displayed for the link, informing users about the destination or action they are about to take.
* Link URL: The URL users are directed to when clicking the Launch Link. If left empty, the link will not be visible. To disable clicking for this item, enter **#** in this field and select the **Redirect to Link URL (Project URL)** option in **Item Linking**.
* **Link Target:** Choose whether the link should open in a new tab or window when clicked.
* **Item Linking:** Instead of directing users to the default portfolio item single page, you can provide an external URL where users will be redirected (optional).

### Checklists

This feature allows you to list works or services associated with the showcase item. It displays entries in specific structure to the **item type** you choose. You can add one or more items, or leave it empty as it is optional. To add a new checklist, click **New Checklist**. A table with three input fields will be displayed:

<figure><img src="../../../.gitbook/assets/Creating a Portfolio Item - Checklists.jpg" alt=""><figcaption></figcaption></figure>

* **Checklist Title:** The title that is displayed for the checklist.
* **Checklist:** The works or services listed as names/titles in lines. These are automatically converted into a list format.
* Column Width: This setting determines the width of the columns for displaying checklists within the container. If multiple checklists are present, this setting applies to all of them.

To delete a checklist, hover over the checklist you want to remove and click the “**minus**” sign on the right.

### Featured Video

You can replace the featured image with a video. If the video is set to autoplay, it will play automatically with overlay information visible. If not, users can start the video manually, which may hide the overlay information. The featured video will be shown only on the **Portfolio Page**, not on the single item page.

<figure><img src="../../../.gitbook/assets/Creating a Portfolio Item - Featured Video.jpg" alt=""><figcaption></figcaption></figure>

* **Featured Video:** Upload the video material by clicking Add Video and then Add File for the video source.
* **Autoplay:** Automatically starts the video when the portfolio item loads (default). If on, the video will be muted automatically, for [this particular reason](https://developer.chrome.com/blog/autoplay).
* **Controls:** Display video controls (play, pause, etc.) for user interaction.
* **Loop:** Automatically restart the video when it finishes.

### Other Settings

Allows you to further customize your portfolio items with options to set a custom hover background color, select the style of the hover overlay, and define the default state of the overlay—whether it should appear on hover, be hidden on hover, or always be visible.&#x20;

These settings apply specifically to the Project Page (portfolio catalog).

<figure><img src="../../../.gitbook/assets/Creating a Portfolio Item - Other Settings.jpg" alt=""><figcaption></figcaption></figure>

* **Custom Hover Background Color**: The color to apply to the hover layer.
* **Hover Effect Style**: Show or hide the entire overlay information, or set a custom style for it.
* **Hover Layer State**: Set the default state for the overlay layer, which can appear on hover, be hidden on hover, or always be visible.

## Setting Up Item Types

With the common settings for portfolio items outlined, we will now explore the detailed settings for each portfolio item type specified in the **Project Layout** tab.

Here are the available item types for the portfolio:

* [**Side Portfolio**](side-portfolio.md)
* [**Columned**](columned.md)
* [**Carousel**](carousel.md)
* [**Zig Zag**](zig-zag.md)
* [**Fullscreen**](fullscreen.md)
* [**Lightbox**](lightbox.md)
* [**Design Your Own**](design-your-own.md)
