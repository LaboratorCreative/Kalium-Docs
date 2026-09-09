---
description: >-
  Small tags that drop dynamic content, the copyright line, social icons, a
  template part, into places that only accept text.
---

# Shortcodes

A shortcode is a short tag in square brackets that WordPress swaps for real content when the page loads. `[year]` becomes 2026. `[kalium_social_icons]` becomes your row of social links.

They're useful wherever you can type text but can't drop in a proper element, a widget, a text field, the middle of a paragraph.

**Two of them are already on your site.** Kalium's default footer is built from `[kalium_site_info]` and `[kalium_social_icons]`, which is why the copyright year updates itself.

***

### Where shortcodes work

| Place | Works |
| --- | --- |
| Post and page content | Yes |
| The builder's **Text** element | Yes |
| Text widgets | Yes, Kalium adds this; WordPress doesn't have it |
| WPBakery text elements | Yes |
| Theme option text fields | Only where the field says so |
| Custom JavaScript fields | No |

Fields that accept shortcodes tell you: *"HTML and shortcodes are supported."*

{% hint style="info" %}
**A shortcode printing as plain text** means the field you put it in doesn't process shortcodes. Move it to page content, a text widget, or a builder Text element.
{% endhint %}

***

## The copyright line

### `[kalium_site_info]`

This is what builds the line at the bottom of your site.

| Attribute | Default |
| --- | --- |
| `display` | `{copyright} {year} {site_title} – {theme_credits}` |

Four placeholders are swapped for real values:

| Placeholder | Becomes |
| --- | --- |
| `{copyright}` | © |
| `{year}` | The current year |
| `{site_title}` | Your site name from **Settings -> General** |
| `{theme_credits}` | "WordPress theme by Laborator", linked |

**To remove the theme credit** while keeping a year that updates itself, use:

```
[kalium_site_info display="{copyright} {year} {site_title}"]
```

Anything that isn't a placeholder is printed as written, so you can put your own wording around them:

```
[kalium_site_info display="{copyright} {year} {site_title}. All rights reserved."]
```

This is the cleanest way to change the footer branding.

{% content-ref url="../general/footer/adding-editing-content.md" %}
[adding-editing-content.md](../general/footer/adding-editing-content.md)
{% endcontent-ref %}

***

## Social icons

### `[kalium_social_icons]`

Shows the accounts you've set once under **Appearance -> Customize -> General -> Social Icons**. The shortcode takes the list from there, the attributes only change how it looks.

| Attribute | Values | Default |
| --- | --- | --- |
| `icon` | `yes` / `no` | `yes` |
| `label` | `yes` / `no` | `no` |
| `spacing` | a number | theme default |
| `size` | a number | theme default |
| `radius` | `rounded`, `square`, or a value | none |
| `outline` | `yes` / `no` | `no` |
| `new_tab` | `yes` / `no` | theme default |
| `no_follow` | `yes` / `no` | theme default |

Six color attributes take either `brand`, each network's own color, or any CSS color:

`color` · `color_hover` · `label_color` · `label_hover` · `background` · `background_hover`

```
[kalium_social_icons icon="yes" label="no" radius="rounded" background="brand"]
```

{% hint style="info" %}
**Nothing appears?** No accounts are set under **Customize -> General -> Social Icons**. The shortcode has no list of its own.

**A color attribute is ignored?** `background` and `outline` need a shape to work with. Set `radius` first.
{% endhint %}

{% content-ref url="social-icons.md" %}
[social-icons.md](social-icons.md)
{% endcontent-ref %}

### `[lab_social_networks]`

The original social shortcode from before Kalium 4.0. **Existing uses keep working**. There's no need to convert them. Use `[kalium_social_icons]` for anything new.

***

## Template parts and snippets

### `[kalium_section]`

Drops a Template Part of type **Section** into content, wherever you put the tag.

| Attribute | Values | Default |
| --- | --- | --- |
| `id` | The template part's ID | `0` |
| `check_conditions` | `yes` / `no` | `no` |

```
[kalium_section id="482"]
```

Display conditions are skipped by default. You're placing it deliberately, so it appears where you put it. Set `check_conditions="yes"` to honor them anyway.

{% hint style="info" %}
**Nothing renders?** The ID must belong to a template part whose Type is **Section**. A Header, Footer, Page or Popup part returns nothing at all.
{% endhint %}

### `[kalium_snippet]`

Runs a Template Part of type **Snippet** inside content. The Template Parts list shows the ready-made tag in its **Shortcode** column.

| Attribute | Values | Default |
| --- | --- | --- |
| `id` | The snippet's ID | `0` |
| `check_conditions` | `yes` / `no` | `no` |
| anything else | Passed to the snippet |, |

```
[kalium_snippet id="512" title="Hello" count="3"]
```

Any extra attribute you add is handed to the snippet's code, which is how one snippet can produce different output in different places.

Only a **published** snippet runs. A disabled one returns nothing.

{% content-ref url="../template-parts/creating-template-parts/code-snippets/" %}
[code-snippets](../template-parts/creating-template-parts/code-snippets/)
{% endcontent-ref %}

***

## Portfolio

### `[kalium_portfolio_share_buttons]`

The share buttons from a portfolio project, usable anywhere.

| Attribute | Default |
| --- | --- |
| `id` | The current post |

Which networks appear, and whether they show as text or icons, both come from **Customize -> Portfolio -> Project Page -> Social Sharing**.

### `[kalium_ajax_like_button]`

The like button with its count.

| Attribute | Default |
| --- | --- |
| `id` | The current post |

Likes are switched on per area, for the portfolio grid that's **Customize -> Portfolio -> Portfolio Page -> Like Feature**.

***

## Dates

### `[date]`

Prints today's date.

| Attribute | Default |
| --- | --- |
| `format` | Your date format from **Settings -> General** |

```
[date format="Y"]
```

That prints just the year, handy in a copyright line.

{% hint style="info" %}
Kalium only registers `[date]` if no plugin has already claimed it. If the output looks unfamiliar, another plugin owns the tag.
{% endhint %}

***

## Video and audio

Kalium takes over WordPress's own `[video]` and `[audio]` shortcodes to use a better player and accept some extra attributes.

| Attribute | Values | Applies to |
| --- | --- | --- |
| `playsinline` | `yes` / `no`, play inline on iPhone instead of going fullscreen | video |
| `object_fit` | `contain` / `cover`, how the video fills its box | video |
| `controls` | `yes` / `no`, lets you hide the controls | both |
| `poster` | An attachment ID as well as a URL | both |

`autoplay` also gains a third value:

**`autoplay="on-viewport"`** starts playback when the video scrolls into view rather than on page load. **This is the one to use**, browsers block most autoplay on load, but allow this.

```
[video src="film.mp4" autoplay="on-viewport" object_fit="cover" playsinline="yes"]
```

**Site-wide settings** live at **Customize -> General -> Media**: which player is used, whether videos autoplay and repeat, and whether YouTube links use YouTube's player or the theme's. An attribute on the shortcode always beats the site-wide setting.

{% hint style="info" %}
**A video won't autoplay.** Browsers block autoplay with sound. Kalium mutes autoplaying video for you, unless you've set `muted="false"` yourself, which stops it starting. Prefer `autoplay="on-viewport"`.

**Every video on the site autoplays.** That's **Customize -> General -> Media -> Autoplay Videos**, not the shortcode.

**The video looks different in the editor than on the site.** Expected, Kalium doesn't theme the editor's preview. Check the front end.

**`[audio]` is tiny.** Without a poster it defaults to a narrow bar. Set a `width`, or give it a `poster` image.
{% endhint %}

***

### When a shortcode doesn't work

**It prints as plain text.**\
The field doesn't process shortcodes. Move it to page content, a text widget, or a builder Text element.

**`[acf]` does nothing.**\
Kalium switches ACF's shortcode off deliberately. Use a builder element or a template part to show a custom field.

**Nothing appears where a shortcode should be.**\
For `[kalium_section]` and `[kalium_snippet]`, check the ID is right and the part is the correct Type and published. A PHP snippet that outputs nothing shows nothing. That's not an error.
