# Popups

Popups are a powerful way to capture visitor attention and drive engagement on your website. Whether you're promoting a sale, collecting newsletter subscribers, displaying important announcements, or presenting exit offers, Kalium's popup system gives you complete control over when, where, and how your popups appear.

### Getting Started

#### Creating a Popup

1. Navigate to **WordPress Admin → Kalium → Template Parts**
2. Click the **Add New** button
3. Select **Popup** as the template part type
4. Design your popup content using your preferred editor:
   * **Gutenberg** (default) - WordPress block editor
   * **Elementor** - If installed and active
   * **WPBakery** - If installed and active
5. Configure the popup settings in the sidebar panels
6. **Publish** when ready

Your popup will automatically appear on your site based on the conditions and triggers you configure.

***

### Settings Panels

The popup settings are organized into panels in the editor sidebar. Each panel controls a specific aspect of your popup's behavior and appearance.

***

### Display Conditions

Control where your popup appears on your website. You can target specific pages, posts, categories, or other conditions to ensure your popup shows only to the right audience.

Read more about [Display Conditions](../settings/display-conditions.md) here.

***

### Popup Triggers

Define what action causes your popup to appear. You can add multiple triggers, and the popup will show when **any one of them** is activated (first match wins).

#### On Page Load

Shows the popup when the page finishes loading.

| Option | Description                                 |
| ------ | ------------------------------------------- |
| Delay  | Seconds to wait before showing (default: 0) |

**Use case:** Welcome messages, cookie notices, or announcements that should appear immediately.

***

#### On Scroll

Shows the popup when the visitor scrolls to a certain position on the page.

| Option          | Description                                        |
| --------------- | -------------------------------------------------- |
| Direction       | Scroll direction to monitor: **Down** or **Up**    |
| Scroll Position | How far to scroll before triggering (default: 50%) |

The scroll position supports different units:

* **Percentage (%)** - Percentage of total page height
* **Pixels (px)** - Fixed pixel distance
* **Viewport Height (vh)** - Percentage of screen height

**Use case:** Show a newsletter signup after visitors have engaged with your content.

***

#### On Scroll to Element

Shows the popup when a specific element becomes visible on screen.

| Option       | Description                                                                |
| ------------ | -------------------------------------------------------------------------- |
| CSS Selector | The element to watch for (e.g., `#contact-form`, `.cta-section`, `footer`) |

**Use case:** Trigger a popup when visitors reach your pricing section or contact form.

***

#### On Click

Shows the popup when the visitor clicks on a specific element.

| Option       | Description                                |
| ------------ | ------------------------------------------ |
| CSS Selector | Element that triggers the popup (optional) |

If no selector is provided, clicking anywhere on the page will trigger the popup.

**Use case:** Create custom buttons or links that open your popup, like "Get a Quote" or "Learn More" buttons.

***

#### After Inactivity

Shows the popup after the visitor has been idle for a period of time (no mouse movement, scrolling, or keyboard activity).

| Option    | Description                                        |
| --------- | -------------------------------------------------- |
| Idle Time | Seconds of inactivity before showing (default: 30) |

**Use case:** Re-engage visitors who may have gotten distracted or are about to leave.

***

#### On Page Exit Intent

Shows the popup when the visitor moves their mouse toward the browser's close/back buttons (top of the viewport). This detects when someone is about to leave your page.

This trigger has no additional options.

**Use case:** Last-chance offers, discount codes, or "Wait! Before you go..." messages.

***

#### Based on Visitor Activity

Shows the popup based on cumulative visitor behavior tracked across their browsing session or multiple visits.

| Activity Type     | Description                                                             |
| ----------------- | ----------------------------------------------------------------------- |
| **Page Views**    | Trigger after viewing X pages (default: 3)                              |
| **Sessions**      | Trigger after X separate browsing sessions (default: 3)                 |
| **Clicks**        | Trigger after X clicks anywhere on the site (default: 3)                |
| **Scroll Amount** | Trigger after scrolling X total pixels across all pages (default: 5000) |

All activity types also support an optional **Delay** setting to wait before showing the popup once the threshold is reached.

**Use cases:**

* Show a special offer to returning visitors (Sessions)
* Reward engaged readers with exclusive content (Page Views)
* Target highly engaged users (Scroll Amount)

***

### Display Frequency

Control how often the popup reappears after a visitor closes it. This prevents annoying repeat displays while still ensuring your message reaches visitors.

| Option               | Behavior                                                    |
| -------------------- | ----------------------------------------------------------- |
| **Once Per Session** | Shows once per browser session (resets when browser closes) |
| **Once Per Day**     | Shows once every 24 hours                                   |
| **Once Per Week**    | Shows once every 7 days                                     |
| **Once Per Month**   | Shows once every 30 days                                    |
| **One Time Only**    | Never shows again after being closed                        |
| **Custom Interval**  | Specify exact seconds between displays                      |

**Tip:** For important announcements, "Once Per Session" works well. For promotional popups, "Once Per Day" or "Once Per Week" is less intrusive.

***

### Layout

Configure the popup's size, position, and visual styling.

#### Size

| Option     | Description                                                                   |
| ---------- | ----------------------------------------------------------------------------- |
| **Width**  | Popup width (default: 60%). Supports responsive values for tablet and mobile. |
| **Height** | Popup height. Leave empty to automatically fit the content.                   |

#### Position

| Option         | Values              |
| -------------- | ------------------- |
| **Horizontal** | Left, Center, Right |
| **Vertical**   | Top, Center, Bottom |

#### Offset

Fine-tune the popup's position from the edges of the screen.

| Option       | Description                       |
| ------------ | --------------------------------- |
| **X Offset** | Horizontal distance from the edge |
| **Y Offset** | Vertical distance from the edge   |

#### Scroll Lock

When enabled, prevents the page from scrolling while the popup is open. Useful for important popups that require user attention.

#### Style

| Option            | Description                                                                                          |
| ----------------- | ---------------------------------------------------------------------------------------------------- |
| **Background**    | Popup background color (supports theme colors)                                                       |
| **Padding**       | Inner spacing around your content. Supports individual values for each side and responsive settings. |
| **Border Radius** | Corner roundness. Supports individual values for each corner.                                        |
| **Box Shadow**    | Drop shadow effect behind the popup                                                                  |

***

### Overlay

Configure the backdrop that appears behind your popup.

| Option              | Description                                                  |
| ------------------- | ------------------------------------------------------------ |
| **Overlay**         | Enable or disable the darkened backdrop                      |
| **Overlay Color**   | Backdrop color with opacity (default: semi-transparent dark) |
| **Background Blur** | Blur the page content behind the overlay (0-10 pixels)       |
| **Close on Click**  | Allow visitors to close the popup by clicking the overlay    |

***

### Closing

Configure how visitors can close the popup.

#### Close Button

| Option                | Description                                           |
| --------------------- | ----------------------------------------------------- |
| **Close Button**      | Show or hide the X button                             |
| **Button Position**   | Inside or Outside the popup                           |
| **Button Size**       | Size of the close button (supports responsive values) |
| **Button Color**      | Icon color for normal and hover states                |
| **Button Background** | Background color for normal and hover states          |

#### Keyboard

| Option           | Description                                  |
| ---------------- | -------------------------------------------- |
| **Close on ESC** | Allow visitors to close using the Escape key |

#### Auto-Close

| Option         | Description                                 |
| -------------- | ------------------------------------------- |
| **Auto Close** | Automatically close the popup after a delay |
| **Delay**      | Seconds before auto-closing (default: 10)   |

**Use case:** Time-limited announcements or messages that should disappear automatically.

***

### Animation

Configure the opening and closing effects for your popup.

#### Animation Type

| Type            | Description                     |
| --------------- | ------------------------------- |
| **None**        | No animation, appears instantly |
| **Fade**        | Smooth opacity transition       |
| **Zoom**        | Scales from small to full size  |
| **Slide Up**    | Enters from the bottom          |
| **Slide Down**  | Enters from the top             |
| **Slide Left**  | Enters from the right           |
| **Slide Right** | Enters from the left            |
| **Bounce In**   | Playful bouncing effect         |

#### Animation Duration

Speed of the animation in seconds (default: 0.3). Lower values create snappier animations, higher values create smoother, slower effects.

***

### Responsive

Control which devices display your popup.

| Option      | Description             |
| ----------- | ----------------------- |
| **Desktop** | Show on desktop screens |
| **Tablet**  | Show on tablet devices  |
| **Mobile**  | Show on mobile phones   |

All devices are enabled by default. Disable any device type to hide the popup on that screen size.

**Tip:** If your popup content doesn't work well on small screens, consider disabling mobile display or creating a separate mobile-optimized popup.

***

### Best Practices

1. **Don't be intrusive** - Use appropriate display frequencies and consider user experience
2. **Time your triggers** - Let visitors engage with your content before showing popups
3. **Keep it focused** - Each popup should have one clear purpose and call-to-action
4. **Test on all devices** - Ensure your popup looks good on desktop, tablet, and mobile
5. **Provide easy exit** - Always allow visitors to close the popup easily
6. **Match your brand** - Use colors and styling consistent with your website design
