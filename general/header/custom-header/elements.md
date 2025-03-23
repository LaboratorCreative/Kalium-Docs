# Elements

Elements are a key part of the Custom Header Builder, and you can include as many as you need.

<figure><img src="../../../.gitbook/assets/Header Elements.jpg" alt="" width="280"><figcaption><p>The list of elements supported in the custom header</p></figcaption></figure>

***

### Menu

Adds a navigational menu to your header, allowing users to access different sections of your site.

<figure><img src="../../../.gitbook/assets/Header Element - Menu.jpg" alt="" width="288"><figcaption></figcaption></figure>

**Menu**\
The navigation menu to show. To create and/or manage menus, go to Appearance -> Menus

**Submenu Arrow**\
Whether to show the arrow indicator for menu items with submenus.

**Mobile Menu Trigger**\
At the mobile menu breakpoint, the navigation hides and a toggle button appears to open the mobile menu.

**Trigger Position**\
Related to the above option (if enabled), this option sets the placement of the trigger button within the current column, allowing it to be positioned at either the beginning or the end.

**Menu Item Spacing**\
The spacing between top-level menu items.

***

### Menu Trigger

Creates a button or icon that toggles a menu type. The available options will depend on the selected menu type.​

<figure><img src="../../../.gitbook/assets/Header Element - Menu Trigger.jpg" alt="" width="286"><figcaption></figcaption></figure>

{% tabs %}
{% tab title="Standard" %}
**Position**\
Will set the placement of navigation within the column.

**Animation**\
The toggle animation of root-level navigation links. It has fade, slide and scale animations available.

**Animation Direction**\
The staggering animation direction of root-level menu items.

**Submenu Arrow**\
Whether to show the arrow indicator for menu items with submenus.

**Menu Item Spacing**\
The spacing between top-level menu items.
{% endtab %}

{% tab title="Fullscreen" %}
**Content Align**\
The placement of the navigation menu determines its layout: the Left and Centered options display menu links as a vertical list, while the Horizontal option arranges menu items in a horizontal row.

**Search Field**\
Optionally, you can add a search bar as the last item in the menu, allowing users to search your site easily.
{% endtab %}

{% tab title="Off-Canvas Side" %}
**Widgets**\
Choose whether to display widgets within the menu container. The widgets displayed here are sourced from the **Off-Canvas Side** sidebar.

**Alignment**\
Adjust the alignment of the menu container, by default opens from right side.
{% endtab %}

{% tab title="Off-Canvas Top" %}
**Items per Row**\
Divides the navigation menu items into columns within each row.

**Widgets** \
Choose whether to display widgets within the menu container. The widgets displayed here are sourced from the **Off-Canvas Top** sidebar.

**Columns** \
Determines how many columns the widgets are divided into.

**Container** \
Defines the size of the widget container relative to the Menu Container.
{% endtab %}
{% endtabs %}

***

### Text

Allows you to insert custom text into your header for announcements, taglines, or other information. It supports shortcodes and HTML as well.

<figure><img src="../../../.gitbook/assets/Header Element - Text.jpg" alt="" width="285"><figcaption></figcaption></figure>

***

### Search Field

Provides a search bar that enables users to search your site directly from the header.

<figure><img src="../../../.gitbook/assets/Header Element - Search Field.jpg" alt="" width="284"><figcaption></figcaption></figure>

**Search Field Alignment**\
The alignment of the input field in relation with the search button (:mag\_right: icon). Useful to avoid search input overflow the container.

**Search Field Visibility**\
By default, the search input is hidden. It will only become visible when users click on the search icon :mag\_right:. If you set the value to **Always**, the search input will remain visible at all times.​

**Icon Animation**\
Applicable when using **On click** search visibility, this setting will apply an animation effect when the search input is focused.

***

### Social Icons

Adds icons linking to your social media profiles, enabling users to connect with you on various platforms.

<figure><img src="../../../.gitbook/assets/Header Element - Social Icons.jpg" alt="" width="283"><figcaption></figcaption></figure>

{% tabs %}
{% tab title="Content" %}
**Icon**\
Controls whether the social network icon is displayed.

**Label**\
Determines whether to display the label alongside the social network icon.

**Spacing**\
The spacing between social network icons.

**Size**\
The size of the social media icon.

**Shape**\
Applies around the icon only. If set to different value than **None**, it will make the icon background rounded, square or any radius you specify.

**Shape Fill**\
If the shape option is applied, you can choose to display it with a solid background or as an outline border.​
{% endtab %}

{% tab title="Links" %}
**Open in New Tab**\
As the name suggests, this option will open the links in a new window or tab.

**Nofollow**\
If checked, prevents search engines from following the link.
{% endtab %}

{% tab title="Colors" %}
Brand colors of social icons are defined in **Appearance -> Customize -> General -> Social Icons**

**Color**\
The color of the icon or label. It can be Brand color, or any custom color you like.\
\
**Hover Color**\
The hover color of the icon or label.

**Label Color**\
If label is set to visible, it will inherit color from previous option, or set custom color for label only.

**Label Hover Color**\
The color to apply on hover for the label only. Inherits the color from Color option by default.

**Background**\
If the shape is applied, then the background color of the shape can be set here.

**Background Hover**\
The hover color of shape background.
{% endtab %}
{% endtabs %}

***

### Button

Inserts a customizable button into your header for calls to action or other important links.

<figure><img src="../../../.gitbook/assets/Header Element - Button.jpg" alt="" width="284"><figcaption></figcaption></figure>

{% tabs %}
{% tab title="Content" %}
**Label**\
The text displayed on the button.

**Link**\
The URL the button directs to.​

**Open in New Tab**\
Whether the link opens in a new window or tab.​
{% endtab %}

{% tab title="Color & Fill" %}
<figure><img src="../../../.gitbook/assets/Header Builder - Button Color.jpg" alt="" width="281"><figcaption></figcaption></figure>

**Background**\
The button background colors for _Normal_, _Hover_, and _Active_ states.

**Text**\
The button text colors for _Normal_, _Hover_, and _Active_ states.

***

<figure><img src="../../../.gitbook/assets/Header Builder - Button Fill.jpg" alt="" width="276"><figcaption></figcaption></figure>

**Fill Type**\
Determines whether the button has an outline or a solid background
{% endtab %}

{% tab title="Layout" %}
**Padding**\
Controls the space inside the button between its content and border.

**Border Radius**\
Sets the roundness of the button’s corners.
{% endtab %}
{% endtabs %}

***

### Date and Time

Displays the current date and time in your header, which can be useful for event-related sites or general information.

<figure><img src="../../../.gitbook/assets/Header Builder - Date and Time.jpg" alt="" width="282"><figcaption></figcaption></figure>

**Date or Time Format**\
Customize the format for displaying date or time. For more details, refer to the [WordPress date format documentation](https://wordpress.org/support/article/formatting-date-and-time/).

***

### My Account

Adds a section for user account management, allowing users to log in or access their account details.

{% hint style="info" %}
Note: The **WooCommerce** plugin is required for this element to function.
{% endhint %}

<figure><img src="../../../.gitbook/assets/Header Builder - My Account.jpg" alt="" width="285"><figcaption></figcaption></figure>

**Login Text**\
Text displayed for guests (users who are not logged in).

**Logged In Text**\
Text displayed for logged-in users.

**Show Icon**\
The account icon displayed to the left of the text.​

***

### Cart Totals

Shows the total amount of items and cost in the shopping cart, ideal for e-commerce sites.

{% hint style="info" %}
Note: The **WooCommerce** plugin is required for this element to function.
{% endhint %}

<figure><img src="../../../.gitbook/assets/Header Builder - Cart Totals.jpg" alt="" width="284"><figcaption></figcaption></figure>

**Total Price**\
Define how the total price is calculated and displayed: cart totals, subtotals, or totals excluding taxes.

**Prefix Text**\
The text shown before the price numbers.

**Hide Empty Cart**\
Hides the element completely when the cart is empty.

***

### Cart

Displays a cart icon with a summary of items, enabling quick access to the shopping cart.

{% hint style="info" %}
Note: The **WooCommerce** plugin is required for this element to function.
{% endhint %}

<figure><img src="../../../.gitbook/assets/Header Builder - Cart.jpg" alt="" width="284"><figcaption></figcaption></figure>

**Icon**\
Choose to show the cart icon or hide it.

**Title**\
Optional text displayed next to the icon.

**Hide when Empty**\
Hides the element completely when the cart is empty.

**Counter Badge**\
Option to display the number of items in the cart.

**Click Action**\
Choose whether clicking the icon shows a mini cart popup or redirects to the cart page.

**Mini Cart - Show On**\
Select the mouse event (**Click** or **Hover**) to display the mini cart popup, applicable when the click action is set to **Show Mini Cart**.

**Mini Cart - Alignment**\
Set the position of the popup relative to the clicked icon.

***

### Language Switcher

Allows users to switch between different languages on your site, useful for multilingual websites.

{% hint style="info" %}
Note: The **WPML** plugin is required for this element to function.
{% endhint %}

<figure><img src="../../../.gitbook/assets/Header Builder - Language Switcher.jpg" alt="" width="285"><figcaption></figcaption></figure>

**Show Flag**\
Choose to display the flag before or after the language name.

**Flag Position**\
Available when **Show Flag** is enabled, this option sets the flag’s placement relative to the language name.

**Show Label**\
The text that displays the language name in the switcher.

**Label Format**\
Choose how language names are displayed, including their native and translated forms

**Skip Missing Translations**\
Skip displaying languages in the list if no translations are available for the current page.

***

### Breadcrumb

Provides a breadcrumb trail that shows the user’s current location within the site hierarchy, improving navigation and user experience.

{% hint style="info" %}
Note: The **Breadcrumb NavXT** plugin is required for this element to function.
{% endhint %}

<figure><img src="../../../.gitbook/assets/Header Builder - Breadcrumb.jpg" alt="" width="283"><figcaption></figcaption></figure>

***

### Common Options

**Visible On**\
Manage the visibility of each header element across different viewports, including Desktop, Tablet, and Mobile. This feature ensures that you can tailor the display of elements based on the user’s device, enhancing the overall user experience.

**Custom CSS**\
Apply additional styling to each element with Custom CSS. This option allows you to add your own custom styles, providing greater control over the appearance and design of header elements beyond the default options

**Style Options**\
All style options are applied from the Style tab in the Header section. The following section will guide you through styling each header element in detail.
