---
description: Mobile menus that won't open, sticky headers that misbehave, and colors that won't apply.
---

# Header and Menu Problems

Menus are the most common thing to go wrong on a site, and mobile menus most of all. Many of the symptoms below were fixed in past Kalium releases, so **updating to the latest version is worth doing before anything else**.

***

### The mobile menu doesn't open, or closes immediately

**Check first:**

1. **Are you up to date?** Several menu bugs have been fixed: a menu not closing when a link is clicked, submenu links following instead of expanding, and invisible hamburger bars.
2. **Is there a JavaScript error?** Open your browser's developer console. This is usually a caching plugin combining scripts.

**The fix:** update Kalium, then clear your caches and switch off **JavaScript combining** and **delay JavaScript** in your optimization plugin to confirm.

Test on a real phone rather than a narrow browser window, some issues only appear with touch input.

***

### The mobile menu appears at the wrong screen width

**Customize -> Header -> Mobile Menu -> Breakpoint** sets the width below which the mobile menu takes over. The default is 768.

Raise it if your menu wraps awkwardly on tablets. Lower it if you have few items and want the full menu on smaller screens.

***

### Mobile menu colors are wrong

Update first. This was fixed more than once, for link colors on certain devices and for the hamburger icon color.

If it persists, check whether **Styling -> Buttons** is bleeding into the hamburger icon. That particular interaction was also a known issue and is resolved in current versions.

***

### The sticky header misbehaves on tablets

Reported most often on iPads, working on desktop and phone but not tablet.

**Check first:** your version. Several sticky header fixes have shipped, including a JavaScript error on pages with no header at all (some landing page plugins), the sticky logo disappearing, and pill colors.

**Then check** **Customize -> Header -> Sticky Header -> Enable On**, tablet can be switched off there independently of the other two.

{% content-ref url="../general/header/sticky-header.md" %}
[sticky-header.md](../general/header/sticky-header.md)
{% endcontent-ref %}

***

### The sticky logo doesn't appear

**A sticky logo needs a normal logo first.** Set one under **Customize -> Styling -> Brand -> Site Logo**, and then **Sticky Header -> Custom Logo** has something to replace.

{% content-ref url="../styling/brand-and-logo.md" %}
[brand-and-logo.md](../styling/brand-and-logo.md)
{% endcontent-ref %}

***

### The top bar won't stick with the header

**Customize -> Header -> Sticky Header -> Sections**\
Set it to **All Rows** rather than **Main Row**.

{% content-ref url="../general/header/top-bar.md" %}
[top-bar.md](../general/header/top-bar.md)
{% endcontent-ref %}

***

### Header colors don't apply, or only in some states

**Every color control here has Normal, Hover and Active states.** Changing only Normal leaves the other two at their old values, which looks like the setting being ignored when you move your mouse over the menu.

**Then check whether a Transparent Header is active** on that page. It has its own set of colors, which start empty and inherit. Any value set there overrides the normal header on those pages.

{% content-ref url="../general/header/transparent-header.md" %}
[transparent-header.md](../general/header/transparent-header.md)
{% endcontent-ref %}

***

### The transparent header spacing is ignored

**This setting is per device.** Set it on the device you're testing on, the desktop value doesn't apply to phones.

Click the mobile icon beside the setting and set the value there.

{% content-ref url="../other/responsive-settings.md" %}
[responsive-settings.md](../other/responsive-settings.md)
{% endcontent-ref %}

***

### The slide direction is being applied to a full-screen menu

**Slide Direction** only applies when **Type** is set to *Slide Menu*. With a full-screen menu it has nothing to do. Update if you're seeing it applied anyway.

***

### The menu disappeared after upgrading from Kalium 3

This is reported regularly. Kalium 4 stores header content differently, and the old settings come through empty.

**The fix** is to rebuild the header in **Customize -> Header**. It's quicker than it sounds, the layouts do most of the work.

{% content-ref url="../getting-started/migrating-from-kalium-3-to-4/" %}
[migrating-from-kalium-3-to-4](../getting-started/migrating-from-kalium-3-to-4/)
{% endcontent-ref %}

***

### The mini cart sits below the hamburger instead of beside it

Try turning **Hamburger Icon Label** off. The label changes how the header flows on narrow screens, and removing it usually brings the cart back into line.

***

### My header settings stopped working entirely

A **Header Template Part** is very likely replacing the header on those pages. Where one applies, the Customizer's header settings no longer govern that page.

Check **Kalium -> Template Parts** for an active Header part whose conditions match.

{% content-ref url="settings-not-applying.md" %}
[settings-not-applying.md](settings-not-applying.md)
{% endcontent-ref %}
