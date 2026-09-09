# Customizer

The Customizer is where you can edit Kalium's look and functionality. It allows you to adjust theme options such as colors, layouts, and widget placements. With real-time previews, you can see how changes affect your site before applying them, making it easy to customize the theme to fit your design preferences.

Changes made in the Customizer can be scheduled and drafted according to your preferences, or published immediately. This feature enables you to plan and prepare updates in advance, ensuring that your site reflects the desired changes at the right time without immediate publication.

### How to Start Customizing

To access the Customizer, simply go to **Appearance** -> **Customize** from the WordPress Admin menu.

<figure><img src="../.gitbook/assets/Customizer Start Page.jpg" alt=""><figcaption><p>The left side are Customizer Sections and Options, right side is the Site Preview frame</p></figcaption></figure>

You can use the search function to quickly navigate to your desired sections or options.

Each control option is self-explanatory, and for additional information, you can hover over the question mark icon <img src="../.gitbook/assets/Customizer Questionmark.jpg" alt="" data-size="line">  to read more about the function of that setting.

Responsive controls are located at the bottom of the Customizer, allowing you to switch between device viewports and preview changes within the site frame.

***

### Responsive Controls

Responsive controls feature an icon representing different device screens.&#x20;

Clicking this icon allows you to switch between viewports such as _Desktop_, _Tablet_, and _Mobile_. Any values you enter are applied specifically to the selected viewport.&#x20;

Values are inherited from _Desktop_ -> _Tablet_ -> _Mobile_, meaning that if you set a value for _Desktop_, it will also apply to _Mobile_ unless you specify a different value for _Mobile_. However, setting a value for _Mobile_ will not override the _Desktop_ or _Tablet_ settings.

{% content-ref url="../other/responsive-settings.md" %}
[responsive-settings.md](../other/responsive-settings.md)
{% endcontent-ref %}

***

### Nothing is saved until you publish

Everything you change is a preview until you click **Publish** at the top. Close the Customizer without publishing and your changes are discarded.

That makes it safe to experiment: open it, change whatever you like, and if you don't like the result, close without publishing.

The arrow beside **Publish** offers two more options:

**Save Draft**\
Keeps your changes without applying them to the live site. Come back later and publish when you're ready.

**Schedule**\
Publishes automatically at a date and time you choose, handy for a seasonal look that should go live at midnight.

***

### Why a setting might not be visible

Kalium hides settings that don't apply yet, which keeps the panels manageable but can be confusing when you're looking for one.

**A setting appears when the setting above it is switched on.** **Sticky Effect** only exists once **Sticky Header** is enabled. **Custom Logo** only once **Sticky Logo** is on. If you can't find something, check the setting directly above where you expect it.

**A whole section can be switched off.** The Portfolio and WooCommerce groups disappear entirely when their feature is inactive, Portfolio under **Kalium -> Settings**, WooCommerce when the plugin isn't active.

**Use the search box.** Typing a few letters of a setting's name is usually faster than clicking through the panels.

{% content-ref url="theme-settings/" %}
[theme-settings](theme-settings/)
{% endcontent-ref %}

***

### The Customizer vs. everything else

Kalium has several places that change how your site looks, and knowing which does what saves a lot of searching:

| Where | What it controls |
| --- | --- |
| **Appearance -> Customize** | How your whole site looks |
| **Kalium -> Settings** | Which features exist at all |
| **Kalium -> Typography** | Fonts and text sizes |
| **Parameters and Options** | Overrides for one single page or post |
| **Kalium -> Template Parts** | Custom sections, headers, footers and popups |

{% hint style="info" %}
**A Customizer setting stopped working on one page?** Check that page's **Parameters and Options** panel, a per-page override beats the site-wide setting.

**On several pages?** A Template Part is probably replacing that part of the site.
{% endhint %}

{% content-ref url="../troubleshooting/settings-not-applying.md" %}
[settings-not-applying.md](../troubleshooting/settings-not-applying.md)
{% endcontent-ref %}

***

### Backing up and moving your settings

**Appearance -> Customize -> Manage Options** exports every Customizer setting to a file, and imports one back.

Use it before making big changes, and when moving a site: **theme settings are stored per site and don't travel with a copy of your files.**

{% content-ref url="../troubleshooting/manage-options-in-customizer.md" %}
[manage-options-in-customizer.md](../troubleshooting/manage-options-in-customizer.md)
{% endcontent-ref %}

***

### If a change doesn't show on the live site

If it looks right in the Customizer preview but not on your actual site, it's almost always caching:

1. Clear your caching plugin, your host's cache, and any CDN
2. Check that CSS/JavaScript optimization isn't serving an older combined file
3. Load the page in a private browsing window

The preview bypasses caching. Your visitors don't.
