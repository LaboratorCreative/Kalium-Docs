# Layouts

In this section, you’ll learn how to create a header using the pre-defined layout types.

Selecting a pre-defined header type only impacts the main row by setting the menu type in use.&#x20;

This approach is based on the original version of Kalium, which users are familiar with for setting up headers. For a more advanced structure, you can always create a [**Custom**](custom-header/) header type, which will be explained in the upcoming article.

***

### Standard

This header type will either show navigation menu with plain links and their sub menus, or the toggle button that shows/hides the links when animation when clicked.

<figure><img src="../../.gitbook/assets/Header - Standard - Options.jpg" alt="" width="323"><figcaption></figcaption></figure>

**Hamburger Menu**\
When checked, the header will include a menu toggle button (alternatively called Hamburger Menu toggle) which will display the navigation links besides the button on the left side.

**Animation**\
This option appears after enabling the Hamburger Menu and controls the animation for showing and hiding the root-level navigation links.

[Standard style options ->](styling.md#menu)

***

### Fullscreen

This header type will display only the Hamburger Menu toggle, which, when clicked, reveals the navigation menu as an overlay with a smooth animation.



<figure><img src="../../.gitbook/assets/Header - Fullscreen - Options.jpg" alt="" width="322"><figcaption></figcaption></figure>

**Content Alignment**\
The placement of the navigation menu determines its layout: the _Left_ and _Centered_ options display menu links as a vertical list, while the _Horizontal_ option arranges menu items in a horizontal row.

**Search Field**\
Optionally, you can add a search bar as the last item in the menu, allowing users to search your site easily.

[Fullscreen style options ->](styling.md#fullscreen-menu)

***

### Off-Canvas Side

This header type displays a [_Hamburger Button_](#user-content-fn-1)[^1] that toggles the menu with a drawer animation from either the left or right side. It can also include widgets in addition to the default navigation.

<figure><img src="../../.gitbook/assets/Header - Off Canvas Side - Options.jpg" alt="" width="328"><figcaption></figcaption></figure>

**Menu**\
The navigation menu to show or hide completely by selecting _(No menu)_ option.

**Widgets**\
Choose whether to display widgets within the menu container. The widgets displayed here are sourced from the **Off-Canvas Side** sidebar.

**Alignment**\
Adjust the alignment of the menu container, by default opens from right side.

**Force Include**\
This option is rarely used, but in case you want the menu to be triggered by a different element on page, you can do so by adding a class `.sidebar-menu-toggle` to the element that will trigger the **Off-Canvas Side** menu.

[Off-Canvas Side style options ->](styling.md#off-canvas-side)

***

### Off-Canvas Top

This header type is similar to previous type which displays a [_Hamburger Button_](#user-content-fn-1)[^1] that toggles the menu from the top of window. It can also include widgets in addition to the default navigation.

<figure><img src="../../.gitbook/assets/Header - Off Canvas Top - Options.jpg" alt="" width="328"><figcaption></figcaption></figure>

**Menu**\
The navigation menu to show or hide completely by selecting _(No menu)_ option.

**Items per Row**\
Divides the navigation menu items into columns within each row.

**Widgets**\
Choose whether to display widgets within the menu container. The widgets displayed here are sourced from the **Off-Canvas Top** sidebar.

**Columns**\
Determines how many columns the widgets are divided into.

**Container**\
Defines the size of the widget container relative to the Menu Container.

**Force Include**\
This option is rarely used, but in case you want the menu to be triggered by a different element on page, you can do so by adding a class `.top-menu-toggle` to the element that will trigger the **Off-Canvas Top** menu.

[Off-Canvas Top style options ->](styling.md#off-canvas-top)

[^1]: toggle button
