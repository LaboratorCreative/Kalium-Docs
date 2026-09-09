# Advanced Settings

Here, you can manage advanced options to customize the font experience, including when to load the font and how to override default font settings. This section is ideal for users who need specific configurations for different parts of their site or want to optimize font loading performance.

***

### Conditional Loading

Configure when to include the font on specific pages, posts, or other post types. You can also exclude it from certain areas if needed:

<figure><img src="../../.gitbook/assets/conditional-font-loading.jpg" alt=""><figcaption></figcaption></figure>

**Every font on a page has to be downloaded before text appears in it.** A font used on one landing page but loaded on all 200 pages of your site is 200 pages paying for something one of them uses.

Conditional Loading fixes that: load the font only where it's needed.

#### When it's worth using

**A display font used on one page.** A bold decorative font on the home page, loaded nowhere else.

**A font for the shop only.** Loaded on product and shop pages, skipped on the blog.

**A font for one language**, on a multilingual site.

#### When to leave it alone

If a font is used across your whole site (your body text, your headings) leave Conditional Loading off. Restricting it just means some pages render with the wrong font until it arrives.

{% hint style="info" %}
**Your font disappeared from some pages?** Check here first. A Conditional Loading rule that's narrower than you meant is the usual cause.
{% endhint %}

***

### Overwrite Font Settings

Manage additional font settings which will overwrite the font settings such as [Font Preload](../typography-settings.md#font-preload) or [Import Font](../typography-settings.md#font-import-placement), you can also set the status of the font from Active to Inactive or vice-versa.

These settings normally come from **Kalium -> Settings -> Typography**, where they apply to every font. This panel lets one font do something different.

#### Font Preload

Tells the browser to start downloading the font immediately rather than waiting until it discovers the text that needs it.

**Worth turning on for the font your visitors see first**\
Your body text, or your main heading font. Preloading everything defeats the purpose, since the browser then has several things all competing to be first.

#### Import Font

Where the font's loading instruction is placed in the page. The site-wide default suits most fonts; change it here only when one font needs to load differently from the rest.

#### Status

**Active** or **Inactive**.

Setting a font to Inactive stops it loading without deleting it, useful for testing whether a font is causing a problem, or keeping a font you may want back later.

{% hint style="info" %}
**Turning a font off is the quickest way to test it.** If a font isn't behaving, set it Inactive and reload. If the problem goes, you've found it. Nothing is lost, set it back to Active.
{% endhint %}

***

### Getting fonts to load faster

If text is slow to appear on your site:

**Reduce the variants you load.** Each weight and style is a separate download. Most sites need Regular and Bold, and nothing else. Loading nine weights when you use two is the most common cause of slow text.

**Turn on Pull Google Fonts** in **Kalium -> Settings -> Typography**. This serves Google Fonts from your own server instead of Google's, which is faster and better for privacy.

**Turn on Font Preload** for the font used above the fold.

**Consider System Fonts** for body text. They load instantly because they're already on the visitor's device.

{% content-ref url="../typography-settings.md" %}
[typography-settings.md](../typography-settings.md)
{% endcontent-ref %}

***

### Common questions

**My font doesn't appear on some pages.**\
A Conditional Loading rule is excluding them.

**My font doesn't appear anywhere.**\
Check its **Status** is Active, that it has at least one selector, and clear your caches.

**Preload isn't making any difference.**\
Preloading helps most when applied to one or two fonts. If every font is preloaded, none of them is prioritized.

{% content-ref url="../../troubleshooting/settings-not-applying.md" %}
[settings-not-applying.md](../../troubleshooting/settings-not-applying.md)
{% endcontent-ref %}
