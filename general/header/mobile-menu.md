# Mobile Menu

The Mobile Menu provides a streamlined navigation experience for smaller screens. It features a collapsible, touch-friendly interface with a hamburger icon that toggles the menu at the defined mobile menu breakpoint.

You can edit the Mobile Menu by going to **Appearance -> Customize -> Header -> Mobile Menu**.​

The menu content is divided into two sections: _Main Content_ and _Footer Content_. This structure allows you to add items to the end of the mobile menu container, making them easily accessible while on mobile devices.

Like other header sections, the mobile menu uses a drag-and-drop interface to organize and structure the menu elements.

The mobile menu offers a slightly smaller selection of elements, as not all elements available in other header sections are supported in the mobile menu.​

<figure><img src="../../.gitbook/assets/Mobile Menu Elements.jpg" alt="" width="268"><figcaption><p>Mobile menu elements</p></figcaption></figure>

To add elements simply click :heavy\_plus\_sign: **Add** link in one of content containers and the list of elements will show up.

***

### Building the menu

The builder here works exactly as it does for the header, so if you've built a custom header you already know it.

#### 1. Add an element

Click **Add** in **Main Content** or **Footer Content** and pick from the list.

**Main Content** is the body of the menu — your navigation, a search field, anything visitors need first. **Footer Content** sits at the bottom of the panel, which is where social icons, a phone number or a language switcher belong.

#### 2. Reorder by dragging

Drag elements within a section, or from one section to the other.

#### 3. Configure an element

Click it, and its settings open beside the canvas.

#### 4. Hide without deleting

Click the :eye: eye icon to switch an element off while keeping it configured.

#### 5. Publish

Changes preview live but aren't saved until you click **Publish** in the Customizer.

{% content-ref url="custom-header/README.md" %}
[README.md](custom-header/README.md)
{% endcontent-ref %}

***

### Vertical Align

Sets where the Main Content sits within the panel: **Top**, **Center** or **Bottom**.

**Top** is the usual choice for a menu with several items. **Center** looks better with a short menu on a full-screen layout, where a few links floating in the middle of the screen reads as deliberate rather than unfinished.

***

### Menu Options

You can adjust the behavior and style of the mobile menu by accessing the options in the Mobile Menu section. Scroll down to the **Menu Options** section to make your changes.:

<figure><img src="../../.gitbook/assets/Mobile Menu Options.jpg" alt="" width="325"><figcaption><p>Menu Options</p></figcaption></figure>

**Type**\
The **Slide Menu** provides a standard mobile menu animation, while the **Full Screen** option offers an alternative way to display the menu across the entire screen.

**Slide Direction**\
This option applies only to the **Slide Menu** type. Choose **Slide Right** or **Slide Left** to set the side the menu slides in from.

**Close Button**\
Adds a close (:x:) button to the menu, and sets where it sits: **None**, **Left** or **Right**. **None** is the default — visitors close the menu by tapping the overlay or the hamburger icon again.

Adding one is worth it on a full-screen menu, where there's no visible overlay to tap.

**Breakpoint**\
The breakpoint at which all menu types become hidden and the mobile toggle button appears, ensuring that only the mobile menu is visible at that viewport and smaller sizes. The default is 768.

Raise it if your menu has many items and starts wrapping on tablets. Lower it if you have few items and want the full menu on smaller screens.

***

### Style Options

Like other header parts, the mobile menu also supports custom styling, offering extensive options for configuring its appearance and design.

<div><figure><img src="../../.gitbook/assets/Mobile Menu Styling - Container.jpg" alt="" width="324"><figcaption><p>Overlay and content container style</p></figcaption></figure> <figure><img src="../../.gitbook/assets/Mobile Menu Styling - Slide Menu Type.jpg" alt="" width="324"><figcaption><p>Slide Menu type style options</p></figcaption></figure></div>

**Overlay**\
The overlay color that covers the screen when the mobile menu is active.

**Overlay Blur**\
Blurs the page behind the overlay. A small amount separates the menu from the page underneath and makes the text easier to read — particularly useful when your overlay color is semi-transparent.

**Content Background**\
Applicable only to the Slide Menu type, this option sets the background color of the menu content container.

**Links**\
The colors for the _normal_, _hover_, and _active_ states of the menu items.

**Text** \
Any text that is not a link inside the menu will be colored with this option.

**Close Button**\
The close button's color, in its _normal_ and _hover_ states. Only appears when **Close Button** is set to Left or Right.

#### Slide Menu Type Options

**Content Max Width**\
The maximum width of the menu container on the screen, ideally set between 50% and 80% of the window width.​

**Item Spacing**\
The spacing between header elements and root-level menu items.​

**Padding**\
Padding applied within the menu container.​

***

### Common questions

**The menu doesn't open, or closes immediately.**\
Usually a caching plugin combining or deferring JavaScript. Switch off **combine JavaScript** and **delay JavaScript execution**, clear caches, and test on a real phone.

**The menu appears at the wrong screen width.**\
That's **Breakpoint**.

**Slide Direction does nothing.**\
It only applies to the **Slide Menu** type. A full-screen menu has no direction to slide from.

**The colors are wrong.**\
Each color control has separate normal, hover and active states — changing only Normal leaves the others as they were.

**The mini cart sits below the hamburger instead of beside it.**\
Try turning **Hamburger Icon Label** off. The label changes how the header flows on narrow screens.

{% content-ref url="../../troubleshooting/header-and-menus.md" %}
[header-and-menus.md](../../troubleshooting/header-and-menus.md)
{% endcontent-ref %}
