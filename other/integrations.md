---
description: >-
  Third-party keys and services Kalium connects to, starting with Google Maps.
---

# Integrations

**Appearance -> Customize -> General -> Integrations** is where Kalium stores keys for outside services.

[TAKE THE SCREENSHOT OF THIS PARTICULAR SECTION AND POST HERE: Appearance -> Customize -> General -> Integrations showing the Google Maps API Key field]

***

### Google Maps API Key

Google requires every website that displays a Google Map to have its own API key. Without one, a map shows as a gray box with a warning across it rather than your location.

Paste your key here and every map on your site uses it, the **Map** element in WPBakery, and anything else that draws a Google map.

#### Getting a key

1. Go to the [Google Maps Platform](https://developers.google.com/maps/documentation/javascript/get-api-key)
2. Create a project and enable the **Maps JavaScript API**
3. Create an API key and copy it
4. Paste it into this field and publish

{% hint style="warning" %}
**Restrict your key to your own domain** in the Google Cloud console. An unrestricted key can be used by anyone who views your page source, and Google bills the key's owner.

Google also requires billing details on the account, though normal traffic for a small site typically falls within their free monthly allowance.
{% endhint %}

***

### If your map shows a gray box

Work down this list:

1. **Is a key entered here?** This is the usual answer.
2. **Is the Maps JavaScript API enabled** for that key's project? A key with the wrong API enabled fails the same way.
3. **Are the key's domain restrictions right?** A key restricted to `example.com` won't work on `staging.example.com`.
4. **Is billing set up** on the Google Cloud account? Google disables keys without it.

The exact reason is usually printed on the gray box itself, or in your browser's developer console.

{% content-ref url="page-builders/wpbakery.md" %}
[wpbakery.md](page-builders/wpbakery.md)
{% endcontent-ref %}

***

### Other integrations

Not everything Kalium works with lives on this screen, most integrations need no key at all and simply activate when their plugin does:

| Plugin | What Kalium adds |
| --- | --- |
| **WooCommerce** | The entire shop option group, header cart elements, product cards |
| **WPML** | The Language Switcher element, and translation of builder content |
| **Breadcrumb NavXT** | Breadcrumbs, with Kalium's styling |
| **Elementor** and **WPBakery** | Kalium's own widgets and elements |
| **ACF Pro** | The Parameters and Options panel |

If a setting looks like it's doing nothing, an inactive plugin is a common cause, the setting stays visible either way.

{% content-ref url="../troubleshooting/settings-not-applying.md" %}
[settings-not-applying.md](../troubleshooting/settings-not-applying.md)
{% endcontent-ref %}
