# Migrating from Kalium 3 to 4

Upgrading from **Kalium 3** to **Kalium 4** is more than just a simple update—it’s a significant leap forward.

Kalium 4 brings many exciting updates that make building your website easier and more powerful. It has faster performance, better customization options, and a simpler, more user-friendly design, making it feel like a brand-new tool that meets today’s web design trends.

With this major upgrade, we’ve also moved from the ThemeForest marketplace to our own dedicated platform. This shift allows us to offer you more pricing options, exclusive deals, and a better user experience. By bringing everything under one roof, we can provide better support and a more personalized approach to your needs. For the reasons behind this change, you can [read more here](https://kaliumtheme.com/platform-change).

In this article, you’ll find step-by-step instructions on how to creata a staging site, migrate your license, access new features, and make the most of Kalium 4.

## 1. Create a Staging Website

The safest way to upgrade is to create a staging copy of your current site. There are several ways to create a staging site, including the following methods:

{% tabs %}
{% tab title="Using WP Toolkit" %}
**Using WP Toolkit**

{% embed url="https://www.youtube.com/watch?v=bKrNZENgils" fullWidth="false" %}

This free and straightforward method allows you to quickly create a staging site by cloning your existing WordPress installation. WP Toolkit manages the process, including copying files and the database, to set up a separate staging environment in few seconds.

1. Log in to **cPanel** and open **WP Toolkit**.
2. Select the WordPress installation you want to create a staging site for.
3. In the **Dashboard** tab click **Clone** link right below the tabs.
4. Clone the site in **staging** subdomain.
{% endtab %}

{% tab title="Using WordPress Plugins" %}
**Using WordPress Plugins**

{% embed url="https://www.youtube.com/watch?v=_YLHGuWf80k" %}

This method involves using plugins to create a staging site and provides a straightforward way to duplicate your site for testing.

Popular plugins for this purpose include:

* **All-in-One WP Migration:** Provides an easy way to export and import your site for staging purposes.
* **UpdraftPlus:** Offers staging features in its premium version.

These plugins handle the duplication process and set up a staging environment efficiently.

{% hint style="info" %}
When creating a staging site from the WordPress admin dashboard, ensure that the necessary PHP limits are configured to prevent the process from failing. This includes increasing the **memory limit**, **max execution time**, and **upload size**.
{% endhint %}
{% endtab %}

{% tab title="Using WP-CLI" %}
**Using WP-CLI**

{% embed url="https://www.youtube.com/watch?t=0&v=Mgsg1LdbiCw" %}

This method is for more advanced users. [WP-CLI](https://wp-cli.org) is a command-line tool for managing WordPress installations. This method automates the process and is ideal for users familiar with command-line interfaces. Unlike some WP plugins, it doesn't require any additional costs.

We'll create a staging site within the same environment as your live site. We assume you have:

* Blank Database: `my_staging_db`
* Live Site Path: `/path/to/live-site/`
* Staging Site Path: `/path/to/staging-site/`

Step-by-Step Process:

1.  Navigate to the Live Site Directory:

    ```sh
    cd /path/to/live-site/
    ```
2.  Copy Files to the Staging Directory:

    ```sh
    cp -r . /path/to/staging-site/
    ```
3.  Export the Live Site Database:

    ```bash
    wp db export /path/to/staging-site/my-exported-db.sql
    ```
4.  Move to the Staging Site Directory:

    ```bash
    cd /path/to/staging-site/
    ```
5.  Remove .htaccess to Avoid Redirection Issues:

    ```bash
    rm .htaccess
    ```
6.  Update the Database details in the Configuration File:

    ```bash
    wp config set DB_NAME my_staging_db
    wp config set DB_USER my_user
    wp config set DB_PASS my_pass
    wp config set DB_HOST localhost
    ```
7.  Import the Live Site Database into the Staging Database:

    ```bash
    wp db import my-exported-db.sql
    ```
8.  Replace All URLs in the Database:

    ```bash
    wp search-replace 'my-live-site.com' 'staging.my-live-site.com'
    ```

And that’s it! Your staging site should now be up and running with the copied content and database from your live site.
{% endtab %}
{% endtabs %}

## 2. Migrate to Kalim 4

Migrating from Kalium 3 to Kalium 4 is designed to be as smooth and straightforward as possible, there are two methods of migrating and updating to Kalium 4: automatic and manual migration.

**Automatic Migration** provides a streamlined process directly within your WordPress dashboard. This method is ideal if you prefer a hassle-free upgrade experience. By following the step-by-step instructions, you can transfer your license and update your theme with just a few clicks.&#x20;

On the other hand, **Manual Migration** offers a more hands-on approach for those who may need or prefer to handle the upgrade process manually. This method involves several steps, including transferring your license and updating the theme manually.&#x20;

{% content-ref url="migrating-automatically.md" %}
[migrating-automatically.md](migrating-automatically.md)
{% endcontent-ref %}

{% content-ref url="migrating-manually.md" %}
[migrating-manually.md](migrating-manually.md)
{% endcontent-ref %}

After transferring your license, you will receive an additional 3 months of support.&#x20;

* **If your support subscription is inactive**, this will give you 3 months of support and updates.&#x20;
* **If you have an active support subscription**, it will be extended by 3 months. For example, if your support ends on January 1, 2025, it will now end on April 1, 2025.

{% hint style="warning" %}
**Important:** Only users who purchased Kalium from ThemeForest **before October 1, 2024**, are eligible to receive an extra 3 months of free support and updates when transferring their license to Kalium 4.
{% endhint %}

After your 3 months of support expire, you can choose to renew your license to continue receiving future updates and support. It’s important to note that renewing your license is not required for your website to continue functioning. Websites built with Kalium will remain fully operational without any issues. However, renewing your license is recommended to maintain access to updates, starter sites, and dedicated support. Without renewal, you may miss out on these benefits, but your website itself will continue to operate smoothly.
