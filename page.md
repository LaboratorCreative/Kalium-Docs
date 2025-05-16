# Page

## Display Conditions

Display Conditions let you control **where** and **when** a Template Part appears on your site.

You can choose specific rules to include or exclude areas of your site, based on page type, user role, WooCommerce state, date, and more. This gives you full control over the visibility of your section, header, footer, or page — without needing to write a single line of code.

***

### How to Add Conditions

While editing a Template Part, click the **Kalium icon** in the top-right corner to open the settings panel.

1. Scroll to the **Display Conditions** section
2. Click **Add Condition**
3. Choose the type of condition (e.g. General Page, Single Post, etc.)
4. Define the rule and select the target

You can add multiple conditions and group them using **AND** and **OR** to create more advanced logic.

> Example: Show a banner only on product pages **AND** for logged-in users

***

### Condition Types

Kalium supports a wide range of condition types grouped by purpose:

#### 1. General Page

* Entire Site
* Front Page
* Blog Page
* 404 Error Page
* Search Page

#### 2. Singular Content

* Single Post (choose individual posts)
* Single Page (choose individual pages)
* Custom Post Type Single (select post type, then specific items)
* Attachment

#### 3. Archive

* Blog Archive
* Date Archive
* Author Archive
* Custom Post Type Archive (choose post type)

#### 4. Taxonomy

* Category Archive (select categories)
* Tag Archive (select tags)
* Custom Taxonomy Archive (choose taxonomy and terms)

#### 5. User

* Logged In
* Logged Out
* User Role (choose from roles like Administrator, Subscriber, Customer, etc.)

#### 6. WooCommerce

* Product Page
* Shop Archive
* Product Category Archive
* Product Tag Archive
* Cart Page
* Checkout Page
* My Account Page

> 💡 WooCommerce-related conditions are only shown when WooCommerce is active.

#### 7. Date & Time

* Specific Date
* Specific Time
* Specific Days (e.g. only on weekends or weekdays)

#### 8. Custom Conditions

* **PHP Callback** – Enter a PHP function that returns true/false
* **Post Meta** – Target based on custom meta field values
* **URL Query String** – Match specific key/value pairs in the URL
* **Referrer URL** – Match based on the referring site or page

***

### Using AND / OR Groups

You can combine conditions using **AND** (all must match) or **OR** (any can match) logic.

Click the toggle at the top of the conditions list to switch between AND and OR grouping.

> Example: Show a section on **product pages OR the blog page**, but not elsewhere

***

### Exclude Rules

You can also exclude specific pages or areas by setting the condition to **“is not”** or clicking **Exclude** next to an item.

> Example: Show everywhere **except** the Checkout page

***

Display Conditions are available for all Template Part types and give you complete flexibility over where your content appears.

← Back to Template Part Settings
