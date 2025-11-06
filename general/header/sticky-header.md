# Sticky Header

The Sticky Header feature allows the header to remain fixed at the top of the page while users scroll. This ensures that essential navigation elements and branding are always visible, providing consistent access to menu options and improving the overall browsing experience on longer pages.

To enable the _Sticky Header_, navigate to **Appearance -> Customize -> Header** and activate the **Sticky Header** option. Click on the option to access and adjust its settings.​

***

### General

Control how your sticky header behaves when scrolling, customize logo appearance, and set responsive options for different devices.

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/Sticky Behavior.png" alt="Sticky Beavior options" width="351"><figcaption><p>Sticky Behavior Options</p></figcaption></figure></div>

#### Sections

Choose which parts of the header become sticky when scrolling down the page.

**All Rows**\
Makes all header rows sticky when scrolling.

**Main Row**\
Only the main header row becomes sticky (default setting).

**Top Row**\
Only the top header row becomes sticky when scrolling.

***

#### Mode

Select the sticky header behavior mode.

**Standard**\
The header remains visible at all times when scrolling down the page.

**Auto Hide**\
The header only appears when users scroll up on the page.

***

#### Effect

Choose an animation effect for when the sticky header appears.

**Available Effects**\
Select from None, Slide, Fade, Slide and Fade, or Slide and Fade Up animations.

> **Note:** Selecting an effect will disable the Progress with Scroll behavior, since the header will automatically appear in its active state.

***

#### Progress with Scroll

This option links the sticky header animation to your scrolling progress.

When enabled, the sticky header will smoothly follow your scrolling. When disabled, it will use a standard animation that plays instantly. This option is only available when Effect is set to "None".

***

#### Animation Duration

Set the length of the animation in seconds when the sticky header appears or hides.&#x20;

**Duration Range**\
You can set values between 0 and 10 seconds. Default is 0.3 seconds.

{% hint style="info" %}
This option appears when Progress with Scroll is disabled or when an Effect other than "None" is selected.
{% endhint %}

***

#### Offset

Controls the distance from the top where sticky behavior begins.

**Input Options**\
You can enter a number in pixels (e.g., 50), or a CSS selector (e.g., .top-header-bar) to set the offset after another element.

***

<figure><img src="../../.gitbook/assets/Sticky Logo Options.png" alt="" width="350"><figcaption><p>Logo Option on Sticky State</p></figcaption></figure>

#### Sticky Logo

Our sticky header implementation allows resizing the current logo when entering the sticky state, or completely switching the logo to another image.

**Shrink Logo**\
Adjust how much the logo shrinks when the header becomes sticky (0-100%). The shrinking percentage is relative to the assigned site logo width.

**Custom Logo**\
To display a different image for the sticky header, enable this option.

**Logo Image**\
When Custom Logo is enabled, select or upload your preferred sticky logo image.

***

<figure><img src="../../.gitbook/assets/Sticky Header - Responsive.jpg" alt="" width="325"><figcaption></figcaption></figure>

#### Responsive

The sticky header also includes responsive options, allowing you to enable or disable it for specific devices.

**Enable On**\
Select which device types will display the sticky header: Desktop, Tablet, and Mobile. All three are enabled by default.

***

***

### Styling

You can apply custom styling for sticky header when it enters the sticky state. Here are the options and their usage:

<div><figure><img src="../../.gitbook/assets/Sticky Header - Style Options 1.jpg" alt="" width="325"><figcaption></figcaption></figure> <figure><img src="../../.gitbook/assets/Sticky Header - Style Options 2.jpg" alt="" width="320"><figcaption></figcaption></figure></div>

#### Container

The container supports standard style options like background, border, and shadow. Padding is applied only to the vertical axis.

#### Other Elements

Additional elements in the sticky header support styling on sticky state and they are:

**Links**\
The colors for the normal, hover, and active states of the menu items.

**Text**\
The color settings for other text elements within sticky header.

**Pill Background and Color**\
If pill navigation is enabled, you can apply custom pill background and text colors for each state of the navigation.
