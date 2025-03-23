# Social Icons

All your social profile links can be added in **Appearance** -> **Customize** -> **General** -> **Social Icons**

More than 40 known social profile links are supported but you can also add your own as well.

### Adding a Social Icon

To add a link click the :heavy\_plus\_sign: **Add** and select the social profile you want to add:



<figure><img src="../.gitbook/assets/Social Icon Add.jpg" alt="" width="326"><figcaption><p>Adding Social Icon</p></figcaption></figure>

{% hint style="info" %}
If the icon does not exist, you can always add your own by going to the end of list and clicking **Custom Icon**
{% endhint %}

Then a new dialog will open where you can add your social profile details:

* **Label** (optional)
* **Link** (required)
* **Color** (optional) - All brands have their official color assigned

<figure><img src="../.gitbook/assets/Social Icon Label and Link.jpg" alt="" width="319"><figcaption><p>Social Icon details</p></figcaption></figure>

You can add as many social icons of the same icon as you want. Dragging them by mouse will allow you to change the order of display.

### Displaying Social Icons

Now that you have created the social networks, you can add them whenever you want, and that is possible in 2 ways:

#### 1. Header Element

In the Header Builder you can add **Social Icons** element, which provides its set of attributes to change the look of social networks:

<figure><img src="../.gitbook/assets/Social Icons Header Element.jpg" alt="" width="326"><figcaption><p>Social Icons element in Header Builder</p></figcaption></figure>

After you add this header element it will display its own options in a new popup dialog where you can change:

* **Display Structure** - Show both icon and label or any of them.
* **Spacing** - Between the social icons.
* **Size** - The size the social icons.
* **Shape** - The surrounding shape of the icon.
* **Responsive Visibility** - Choose the viewport where the element will be visible.
* **Colors** - Set colors for the icon, label and shape.

#### 2. Shortcode

The shortcode can be used for places where you are not able to add social icons using standard user interface for inserting Social Icons. Here is the definition of the shortcode and all its available attributues:

```
[kalium_social_icons label="yes" icon="no" spacing="30"]
```

* **label**\
  Allowed values: _yes_, _no_
* **icon**\
  Allowed values: _yes_, _no_
* **spacing**\
  Allowed values: _numeric_, _numeric with unit_ example _1.5em_
* **size**\
  Allowed values: _numeric_, _numeric with unit_ example _1.5em_
* **radius**\
  Allowed values: _rounded_, _square_, _numeric_, _numeric with unit_ example _1.5em_
* **outline**\
  Allowed values: _yes_, _no_ (only set when you add _**radius**_ attribute)
* **new\_tab**\
  Allowed values: yes, no
* **no\_follow**\
  Allowed values: yes, no
* **color**\
  Allowed values: _brand_ (the official color of the brand), _#ffffff_ (any hexadecimal color)
* **color\_hover**\
  Allowed values: _brand_, _any hexadecimal color_
* **label\_color**\
  Allowed values: _brand_, _any hexadecimal color_
* **label\_color\_hover**\
  Allowed values: _brand_, _any hexadecimal color_
* **background**\
  Allowed values: _brand_, _any hexadecimal color_ (applied in combination with radius attribute)
* **background\_hover**\
  Allowed values: _brand_, _any hexadecimal color_ (applied in combination with radius attribute)

Here is a fully featred example that combines all of these shortcode attributes:

```
[kalium_social_icons icon="yes" label="no" spacing="1.5rem" size="30" radius="20px" outline="no" new_tab="yes" no_follow="yes" color="brand" color_hover="#ffaa00" background="yellow" background_hover="#24b4a2"]
```
