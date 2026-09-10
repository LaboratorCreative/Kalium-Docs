---
description: The look of every form field, from contact forms to checkout.
---

# Forms

Manage the appearance and layout of forms across your entire site to maintain a consistent design. This applies to all forms, including contact forms, search forms, comment sections, checkout pages, and more. You can customize the form styles under **Appearance** -> **Customize** -> **Styling** -> **Forms**.

<figure><img src="../.gitbook/assets/forms.jpg" alt=""><figcaption></figcaption></figure>

### General

The General tab lets you control the overall layout and style of forms across your site. This tab includes options to choose the layout type and activate the legacy form style if needed.

#### Form Layout

This section lets you select the basic structure of your forms. You can choose between two layout types:

<figure><img src="../.gitbook/assets/forms-layout.jpg" alt="" width="345"><figcaption></figcaption></figure>

#### Type 1

The default form layout option. This style features a boxed layout, providing a traditional and structured appearance for your forms.

#### Type 2

A more minimalistic layout option where form fields appear as underlined rather than boxed. This style gives your forms a modern and sleek look.

{% hint style="info" %}
**Legacy Form Style**\
This toggle is available for users who have migrated from Kalium 3 and want to continue using the old Kalium forms. However, it's not recommended to use this option as it is considered legacy and will be removed in future updates.
{% endhint %}

***

### Style

In the Style tab, you can customize various aspects of the form fields:

#### Input & Textarea

<figure><img src="../.gitbook/assets/forms-inputs.jpg" alt="" width="341"><figcaption></figcaption></figure>

* **Placeholder**: Set the text color for the placeholder in form fields.
* **Text**: Customize the text color for three states, Normal, Hover and Focus.
* **Background**: The field background for the same three states. Type 1 only.
* **Border**: Define the border color for the three states, Normal, Hover and Focus.
* **Border Width**: Adjust the thickness of the border around form fields.
* **Padding**: Control the space inside the form fields to adjust the size and spacing of the text.
* **Border Radius**: Set how rounded the corners of the form fields are.

#### Box Shadow

Add a shadow effect to the form fields to give them depth and make them stand out, available for the three states (Normal, Hover and Focus).

<figure><img src="../.gitbook/assets/forms-boxshadow.jpg" alt="" width="339"><figcaption></figcaption></figure>

{% hint style="info" %}
Some style settings are hidden when using Type 2, as it lacks a regular border: **Background**, **Border Radius** and the three **Box Shadow** settings appear only for Type 1.
{% endhint %}

#### Textarea

<figure><img src="../.gitbook/assets/forms-textarea.jpg" alt="" width="340"><figcaption></figcaption></figure>

* **Height**: Set the height of the textarea field to control how much text space is available.

#### Checkbox and Radio

<figure><img src="../.gitbook/assets/forms-checkbox.jpg" alt="" width="337"><figcaption></figcaption></figure>

* **Checked**: Define the color that appears when a checkbox or radio button is selected.
* **Border Radius**: Set the roundness of the checkbox and radio button corners.

### Will Form Styling Apply to Other Form Plugins?

Kalium has been tested with the most well-known form plugins to ensure a seamless design experience. The theme styles the form fields themselves, so its styling reaches any plugin's fields as long as the plugin is not painting over them.&#x20;

That is what the plugin's own setting decides. Select the **Theme Styled** option, or the nearest equivalent, in your form plugin settings so it stops applying its own field styles and Kalium's come through.

The supported plugins include&#x20;

* Contact Form 7
* WPForms
* Fluent Forms
* Forminator
* Ninja Forms
