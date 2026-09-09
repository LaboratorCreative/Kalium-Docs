# In Page Options

The **In Page Options** for headers allow you to customize the appearance and functionality of headers on individual pages, posts, or custom post types like Products and Portfolios.&#x20;

This means you can tailor the header settings for each specific page or post, rather than applying a global header style across your entire site. This feature provides flexibility to adjust the header layout, visibility, and other settings to match the unique needs of each content type.

The options you set for specific page[^1], will always take precedence over those configured in the Customizer.

By using these options, you can create a more personalized and cohesive look for different sections of your site, enhancing the overall user experience.&#x20;

To edit header options, in the post editor page, go to **Parameters and Options** -> **Page Options** then the header settings are split in two tabs: **Header Options** and **Logo & Menu** as shown below:

<figure><img src="../../.gitbook/assets/In Page Header Options.jpg" alt=""><figcaption><p>In Page header options</p></figcaption></figure>

### Header Options

In this tab, you can customize the header container and apply your preferred styling options.​

#### Header Position

Set the header position in relation with the page content, for example if you have a slider and want to show the header container over the slider/image then choose **Over the Content** (Absolute) otherwise the default option **Content Below (Static)** is applied.&#x20;

This behavior can be adjusted in global site level by going to **Appearance -> Customize -> Header** and toggling **Transparent Header** option:

<figure><img src="../../.gitbook/assets/Transparent Header.jpg" alt="" width="327"><figcaption></figcaption></figure>

When you select the **Over the Content** option, the **Header Spacing** setting will become available. This option allows you to adjust the spacing for the content that now extends from the very top of the page. This ensures that the content does not overlap with the header and maintains a clean and organized layout.

#### Full Width Header

As the name suggests, this option sets the header to span the full width of the page.

#### Header Styling

Enabling this option allows you to override the header style. Once you select **Yes**, all available [header style options](styling.md) as defined in the Customizer will become available.

<div><figure><img src="../../.gitbook/assets/In Page Header Options - Header Style 1.jpg" alt="" width="375"><figcaption></figcaption></figure> <figure><img src="../../.gitbook/assets/In Page Header Options - Header Style 2.jpg" alt="" width="375"><figcaption></figcaption></figure> <figure><img src="../../.gitbook/assets/In Page Header Options - Header Style 3.jpg" alt="" width="375"><figcaption></figcaption></figure></div>

### Logo & Menu

This tab allows you to change the logo and adjust menu options, including the ability to enable or disable the sticky header.

<figure><img src="../../.gitbook/assets/In Page Header Option - Logo and Menu.jpg" alt=""><figcaption><p>Logo and Sticky Header settings</p></figcaption></figure>

#### Custom Logo

This option lets you set a unique logo for this specific page, overriding the default logo used throughout the site. It’s ideal for giving this page a distinct look while keeping the rest of your site consistent.

#### Custom Logo Width

An optional setting to adjust the width of the custom logo on this page. Leaving it empty will retain the logo’s original dimensions.

#### Sticky Header

Enable or disable the sticky header for this specific page. If Enabled, it will display [style options](sticky-header.md#styling) for sticky header as defined in Customizer.

#### Custom Sticky Logo

Set a different logo to display when the header is in the sticky state.

#### Sticky Header Style

Visible when **Sticky Header** is set to **Enable**. These style options will override the sticky header settings configured in the Customizer.

<div><figure><img src="../../.gitbook/assets/In Page Header Options - Sticky Style 1.jpg" alt="" width="375"><figcaption></figcaption></figure> <figure><img src="../../.gitbook/assets/In Page Header Options - Sticky Style 2.jpg" alt="" width="375"><figcaption></figcaption></figure></div>

#### Logo Switch

This option allows you to change the logo as the header becomes sticky while scrolling down the page. When enabled, you can add multiple logo switch sections by clicking **Add Logo Switch Section** to specify different logos for various scroll positions:

<figure><img src="../../.gitbook/assets/In Page Header Options - Logo Switch On Section.jpg" alt=""><figcaption><p>Logo Switch on Section settings</p></figcaption></figure>

**Switch Type**\
Choose between using a specific section (container) or a Revolution Slider item to trigger the change of the sticky header logo. If you select the Revolution Slider option, a list of sliders will be available. The sticky header logo will update when the slider reaches the top of the viewport.

**Section ID**\
When the switch type is set to **Section**, you need to assign an ID to the parent container of the section that triggers the logo change. This allows the sticky header script to recognize the section and update the logo when it fully enters the viewport.

**Logo**\
Set the logo to be used specifically for this section.

**Logo Width**\
Specifies the width for the logo. By default, the logo will use its original dimensions unless you set a custom width.​

**Transparent**\
Enabling this option will remove the background of the header, making it transparent.

[^1]: or any singular item such as: post, product, portfolio, etc.
