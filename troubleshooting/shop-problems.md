---
description: Add to cart, the cart drawer, product galleries and pagination.
---

# Shop Problems

Many shop issues below were fixed in past Kalium releases, so **update to the latest version first**, it resolves a good proportion of them outright.

{% hint style="info" %}
**Payments, shipping, tax and stock are WooCommerce's own settings**, under **WooCommerce -> Settings**. Kalium controls how the shop *looks*, not how it processes orders. If something isn't working about an order, check WooCommerce first.
{% endhint %}

***

### Add to Cart does nothing

**Check first, in order:**

1. **Is Catalog Mode on?** **Customize -> WooCommerce -> Product Catalog -> Catalog Mode** turns your shop into a browsable catalog with no buying. If it's on, this is the setting working as intended.
2. **Are you up to date?** This was fixed for sites with WooCommerce's AJAX add-to-cart disabled, and again for the cart drawer not opening.
3. **Is there a JavaScript error?** Check your browser console. Usually script combining in an optimization plugin.

***

### Add to Cart is disabled for logged-out visitors only

This isn't a Kalium setting. Check WooCommerce, and any membership or wholesale plugin, for a "must be logged in to purchase" option.

***

### The cart drawer doesn't open or close

**Check first:** **Customize -> Header -> Cart -> Click Action**. If it's set to *Go to Cart Page*, there's no drawer at all. That's by design.

If it's set to open the drawer and nothing happens, update Kalium. This was fixed for the drawer not opening from a product page, and for it not closing after a quantity change.

{% content-ref url="../post-types/woocommerce/general-settings/mini-cart.md" %}
[mini-cart.md](../post-types/woocommerce/general-settings/mini-cart.md)
{% endcontent-ref %}

***

### The column switcher doesn't work

Update. This was fixed twice.

{% hint style="info" %}
**Product Columns** and **Masonry Mode** are hidden when **Columns Switcher** is off, because they depend on it. If those settings have disappeared, that's why.
{% endhint %}

***

### Grid columns are wrong on mobile

**Product Columns is per device.** Click the mobile icon beside the setting and set the value explicitly, the desktop count doesn't carry down.

{% content-ref url="../other/responsive-settings.md" %}
[responsive-settings.md](../other/responsive-settings.md)
{% endcontent-ref %}

***

### Pagination loses my filters, or shows pages that don't exist

Update first. This was fixed for compatibility with Product Filters for WooCommerce, for the mobile pagination layout, and for a hover overlay covering the pagination and blocking clicks.

If it persists, filtered pagination depends on your **filter plugin** generating proper page addresses. Check that plugin's own settings.

***

### Product images don't load on the first visit

A timing issue, fixed in a past release. Update.

***

### The product gallery looks wrong

**Check first:** which **Shop Single Gallery Type** is selected. Each shows a different set of settings, and most of the screen is hidden when *Simple* is chosen.

Known issues that have since been fixed include vertical gallery thumbnails on mobile and a gap in vertical carousel mode, so update if you see either.

{% hint style="info" %}
**If the product page uses Elementor's page template**, Kalium deliberately hands the gallery over to WooCommerce's own, because Elementor's product widget expects that markup. This is intended. To keep Kalium's gallery, use a Kalium page template for products instead.
{% endhint %}

{% content-ref url="../post-types/woocommerce/product-images.md" %}
[product-images.md](../post-types/woocommerce/product-images.md)
{% endcontent-ref %}

***

### Cart totals don't update when the quantity changes

Fixed in a past release. Update.

***

### The My Account or password reset form is broken

Both were fixed, the reset password layout when the My Account image was enabled, and the login form not being visible by default. Update.

{% content-ref url="../post-types/woocommerce/my-account.md" %}
[my-account.md](../post-types/woocommerce/my-account.md)
{% endcontent-ref %}

***

### Product borders look wrong after a WooCommerce update

Fixed after WooCommerce 10. Update Kalium.

***

### The free shipping bar never appears

It needs three things, and all three must be true:

1. A **free shipping method** set up in WooCommerce
2. A **minimum order amount** on that method
3. The current page ticked under **Locations to Show**

{% content-ref url="../post-types/woocommerce/general-settings/free-shipping-bar.md" %}
[free-shipping-bar.md](../post-types/woocommerce/general-settings/free-shipping-bar.md)
{% endcontent-ref %}

***

### The WooCommerce options are missing from the Customizer

WooCommerce isn't active. It's the only option group that disappears entirely when its plugin is inactive.

***

### The cart is missing from the header

Either WooCommerce isn't active, or **Hide when Empty** is on and your cart is empty. Add something to the cart to check.
