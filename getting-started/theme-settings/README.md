---
description: >-
  Kalium -> Settings is where whole features are switched on and off, separate
  from the Customizer, which decides how they look.
---

# Theme Settings

Kalium has two places where you change things, and knowing which is which saves a lot of hunting.

**The Customizer**, **Appearance -> Customize**, decides how your site *looks*. Colors, fonts, header layout, the shop grid.

**Theme Settings**, **Kalium -> Settings**, decides which features *exist*. Whether Template Parts is available at all, whether the portfolio module is loaded, whether backups are taken before updates.

Put simply: the Customizer styles a feature, Theme Settings decides whether there is a feature to style.

[TAKE THE SCREENSHOT OF THIS PARTICULAR SECTION AND POST HERE: the Kalium -> Settings screen showing the section navigation down the side]

***

### The five sections

| Section | What it controls |
| --- | --- |
| **Template Parts** | Whether the Template Parts system is available, and how Snippets are stored and guarded |
| **Portfolio** | The portfolio module, and which post types can use it |
| **Typography** | How fonts load, and the font defaults |
| **Theme Backups** | Automatic backups taken before theme updates |
| **White Label** | Replacing Kalium's branding with your own |

{% content-ref url="template-parts.md" %}
[template-parts.md](template-parts.md)
{% endcontent-ref %}

{% content-ref url="portfolio.md" %}
[portfolio.md](portfolio.md)
{% endcontent-ref %}

{% content-ref url="theme-backups.md" %}
[theme-backups.md](theme-backups.md)
{% endcontent-ref %}

{% content-ref url="white-label.md" %}
[white-label.md](white-label.md)
{% endcontent-ref %}

The **Typography** section is covered with the rest of the typography system, since its settings only make sense alongside it:

{% content-ref url="../../typography/fonts/advanced-settings.md" %}
[advanced-settings.md](../../typography/fonts/advanced-settings.md)
{% endcontent-ref %}

***

### Why a menu or a screen might be missing

Most "where did that go?" questions about the Kalium admin are answered on this screen. Before assuming something is broken, check here:

**The Template Parts menu is gone.**\
Template Parts is switched off, or **Hide Template Parts** is on under White Label.

**The Portfolio options vanished from the Customizer.**\
**Portfolio Extension** is off, or the post type was unticked under **Portfolio Post Types**.

**A dashboard page is missing**, Plugins, Starter Sites, Status, Changelog or Account.\
Check the Hide switches under White Label.

**None of my snippets run, but they're all published.**\
**Snippets Safe Mode** is on.

**I can't find the White Label section.**\
Either your license doesn't include it, or **Hide White Label Settings** is on.

{% hint style="info" %}
Turning a feature off never deletes anything. Your template parts, portfolio items and settings all stay where they are, and come back when you switch the feature on again.
{% endhint %}
