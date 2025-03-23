# Bad Hosting Environment

### Understanding the Pitfalls of Bad Hosting Environments

The title might seem a bit strong, but it's grounded in our extensive experience with customers whose hosting environments didn't meet even the minimal requirements for a WordPress site. Inadequate hosting can cause a range of issues that severely impact your website's performance, stability, and security.

#### Memory Limit

Memory limit is a crucial factor, especially when importing theme demo content or managing your site on a daily basis. Insufficient memory can lead to significant problems like data processing failures, issues with skin compiling, and other server memory-intensive tasks.

#### PHP Configuration Editing

To increase the memory limit and adjust other [recommended PHP configuration settings](../getting-started/introduction/before-getting-started/server-requirements.md), you need access to the `php.ini` file via FTP or directly through cPanel. Some hosting providers also allow PHP configuration through the `.htaccess` file (applicable on Apache servers):

```apache
#format
php_value setting_name setting_value

#example
php_value memory_limit 128M
```

However, not all hosting companies provide the ability to modify these values.

#### Restricted External URL Access

Some hosting providers may restrict external URL access via [cURL](https://www.php.net/manual/en/book.curl.php), which can make our API server inaccessible. This restriction can prevent theme activation, theme updates, and starter sites import for Kalium. Although this is uncommon, it's essential to verify with your hosting provider that requests to `kaliumtheme.com` are allowed.

#### What Should I Do?

Choosing the right [hosting provider](https://kaliumtheme.com/recommendations/) is crucial to ensure smooth website operation. If you're experiencing issues, open a support ticket with your hosting company and ask for help meeting these basic requirements. In some cases, you may need to upgrade your hosting plan to resolve these issues.

{% hint style="info" %}
Please read the [Recommended PHP configuration limits](../getting-started/introduction/before-getting-started/server-requirements.md) article for more details.
{% endhint %}
