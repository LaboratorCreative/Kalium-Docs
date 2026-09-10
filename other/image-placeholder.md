---
description: What visitors see while an image is still loading.
---

# Image Placeholder

Images are crucial to your website’s user experience, and how they’re presented can significantly impact it.

Kalium wraps images in a placeholder container that can have custom style, which is visible before the image is loaded. This is an indicator that _something is loading_ and you can use your own creativity to make the loading state of images as better as possible.&#x20;

Optionally, you can add your own brand logo or custom icon as loading indicator.

To edit these options go to **Appearance** -> **Customize** -> **General** -> **Image Placeholder**

There you can choose between three types of loading types, the default is **Plain Color**:

<figure><img src="../.gitbook/assets/Image Placeholder Types.jpg" alt="" width="338"><figcaption><p>Choose your preferred loading indicator</p></figcaption></figure>

Depending on the type of indicator you choose, relative options will be shown and here what they do:

* **Background** - You can set any color, gradient or the dominant color of the image.
* **Loading Animation** - a CSS loading indicator shown in the middle of image: _Modern Circular_, _Ball Scale_, _Line Scale_, _Ball Pulse_ or _Semi Circle Spin_, with its own **Loader Color**.
* **Custom Image/Icon** - The image you want to show as a loading indicator.

Both the animation and the custom icon share **Alignment**, **Animation Icon Size**, and a **Padding** that appears once Alignment is anything but centered.

### Common Options

Apart from their type, each type of image placeholder will have a background which can be one of the following:

* **Plain color** - Just as name explains it.
* **Gradient** - Choose between two colors and set the angle and the type of gradient.
* **Dominant Image Color** - This will assign custom color for every image based on their dominant color extracted using PHP to get the main color of the image.

### Setting Custom Icon

1. Choose **Custom Icon** from **Image Loading Placeholder Type**
2. Click **Custom Image/Icon** box and select your loading indicator image
3. Set the desired **Alignment** inside box
4. Set **Animation Icon Size** for the image/icon
