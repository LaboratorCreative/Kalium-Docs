# Colors

Colors are a fundamental aspect of the theme, and understanding how to work with them will help you achieve the best results and enhance your site’s overall appearance.

To manage and edit colors go to **Appearance** -> **Customize** -> **Styling** -> **Colors**

***

### Base Palette

The color palette defines the base colors of your site based on your brand guidelines.

It is a set of of **8 colors** by default but you can add more colors by clicking the :heavy\_plus\_sign: icon in upper part of colors strip.

Base palette colors are utilized to be used throughout all color pickers as references so when you update a color in the base palette, every other reference is updated automatically as well.

You can also choose from predefined palettes by clicking the :art: palette icon.

<figure><img src="../.gitbook/assets/Colors Palette.jpg" alt="" width="327"><figcaption><p>Default Color Palette</p></figcaption></figure>

When the colors are modified, the :pencil2: icon will show up instead of the :heavy\_plus\_sign: icon where you can save the current set of colors as a palette:

<figure><img src="../.gitbook/assets/Save as Palette.jpg" alt="" width="324"><figcaption><p>Custom colors can be saved as new palette</p></figcaption></figure>

After you save the palette, it appears in the list of **Custom Palettes** as **Palette X** where X is an ordered number:

<figure><img src="../.gitbook/assets/Saved Palettes.jpg" alt="" width="333"><figcaption><p>List of theme defined palettes with custom user palettes</p></figcaption></figure>

You can also export or import existing palettes including current colors in the same dialog by clicking **Export/Import** tab:

<figure><img src="../.gitbook/assets/Import Export Palettes.jpg" alt="" width="331"><figcaption><p>Export and/or Import current palette colors and custom user palettes</p></figcaption></figure>

***

### Global Theme Colors

Theme palette colors are also recognized by both the Gutenberg and Elementor. This ensures consistency across your site’s design, allowing you to seamlessly apply your chosen color palette in different parts of your site, whether you’re using the Gutenberg blocks or Elementor’s widgets.

<figure><img src="../.gitbook/assets/Gutenberg Base Palette.jpg" alt="" width="255"><figcaption><p>Gutenberg Color Palette</p></figcaption></figure>

<figure><img src="../.gitbook/assets/Elementor Base Palette.jpg" alt="" width="295"><figcaption><p>Elementor Color Palette</p></figcaption></figure>

***

### Global Colors

* **Links** - Normal and hover color for every link in the theme.
* **Text** - Default text color and muted text color.
* **Text Selection** - Change how selected text looks when selected.

***

### Headings

* **Headings H1-H6**  - Default colors for all headings (as every heading size inherits from this value).
* **Heading 1** to **Heading 6** - Custom color for every heading size.

***

### Other Colors

* **Footer** - Footer background, text, headings and link colors.
* **Site Background** - The body background color.
* **Overlay** - Default color of backdrop overlays for lightboxes.

### CSS Color References

Every color provides a CSS variable reference of this form you can use throughout the site:

```css
var(--k-color-1)
var(--k-color-2)
var(--k-color-3)
var(--k-color-4)
var(--k-color-5)
var(--k-color-6)
var(--k-color-7)
var(--k-color-8)
var(--k-color-9) /* custom added colors */
```

As well as their RGB variant:

```css
var(--k-color-1-rgb)
var(--k-color-2-rgb)
var(--k-color-3-rgb)
var(--k-color-4-rgb)
var(--k-color-5-rgb)
var(--k-color-6-rgb)
var(--k-color-7-rgb)
var(--k-color-8-rgb)
var(--k-color-9-rgb) /* custom added colors */
```

So you can use with custom opacity for example:

```css
background: rgba(var(--k-color-1-rgb), 0.5);
```
