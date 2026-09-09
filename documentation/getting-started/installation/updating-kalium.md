# Updating Kalium

Updating Kalium is a simple process, similar as with any other WordPress theme. By keeping your theme up to date, you ensure you have the latest features, improvements, and security updates. Follow these simple steps to update your theme:

### 1. Check for Updates:

* Log in to your WordPress dashboard
* Go to **Dashboard** -> **Updates**
* If a new version of Kalium is available, it will be listed here

### 2. Update the Theme:

* In the Updates section, select Kalium and click **Update Themes**
* Alternatively, go to **Appearance** -> **Themes**, find Kalium, and click **Update Now** if an update is available

{% hint style="info" %}
Make sure your Kalium theme license is active, as it is necessary to download and install updates, and if it is expired, renew it through your account on the [Kalium](https://kaliumtheme.com) website.
{% endhint %}

### 3. Verify the Update:

After update completes, check your website to ensure everything is working correctly.

### Optional: Manual Update

Manual updates should be avoided as the automatic update process is preferred for a smoother and more reliable experience.&#x20;

The manual method requires more steps, including downloading the theme and uploading it via the WordPress admin panel or FTP, which can increase the risk of errors and complicate the update process.

#### Manual Update via WordPress

1. Go to [Kalium Account](https://kaliumtheme.com/account) page and login
2. Go to **Downloads** tab and click **Download** button
3. Go to **Appearance** -> **Themes**
4. Click **Add New Theme** button in the upper part of the page
5. Then click **Upload Theme** button and the upload form will be shown
6. Select or drag the downloaded archive file **kalium.\[version].zip**
7. Replace current version of the theme by clicking **Replace active with uploaded**
8. Theme is updated!

#### Manual Update via FTP

1. Go to [Kalium Account](https://kaliumtheme.com/account) page and login
2. Go to **Downloads** tab and click **Download** button
3. Delete the existing `kalium` folder inside `~/wp-content/themes`
4. Extract the zip file and upload it to your WordPress theme directory [via FTP](installing-theme-via-ftp.md)
5. Theme is updated!

### Important Notes & Best Practices

#### Backup the theme

Whenever you update the theme, it’s essential to ensure that you have an up-to-date backup of your website and database, in case of errors or unwanted results.

Our theme automatically creates a backup of the previous theme version (files only) during the update process. This feature is enabled by default in **Kalium** -> **Settings** -> **Theme Backups**.

#### Clear the caches

It is always recommended to clear your browser cache, any caching plugins, and server cache after updating. Old cached files can cause visual issues or other problems following an update. Clearing your cache ensures that these issues are avoided and that your site reflects the latest changes.

