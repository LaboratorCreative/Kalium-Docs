# Activation Scope

Understanding the activation scope of Kalium is crucial for selecting the plan that best fits your needs. This article will help you determine what constitutes an active installation and how the licensing mechanism supports different activation instances.

An active installation refers to the number of live websites where Kalium has been activated using the license. Each plan specifies a limit on the number of sites where the theme can be activated. This limit ensures that the license is used in accordance with the terms of the selected plan.

### Staging Environment

To support development and testing, the licensing mechanism allows for a staging environment that is not counted towards your activation limit. This means you can set up a staging site for testing or development purposes without affecting the number of active installations covered by the license.

#### TLDs that are considered as dev or staging <a href="#tlds_that_are_considered_as_dev_or_staging" id="tlds_that_are_considered_as_dev_or_staging"></a>

* `*.dev`
* `*.dev.cc` (DesktopServer)
* `*.test`
* `*.local`
* `*.staging`
* `*.example`
* `*.invalid`
* `*.myftpupload.com` (GoDaddy)
* `*.cloudwaysapps.com` (Cloudways)
* `*.wpsandbox.pro` (WPSandbox)
* `*.ngrok.io` (tunneling)
* `*.mystagingwebsite.com` (Pressable)
* `*.tempurl.host` (WPMU DEV)
* `*.wpmudev.host` (WPMU DEV)
* `*.websitepro-staging.com` (Vendasta)
* `*.websitepro.hosting` (Vendasta)
* `*.instawp.xyz` (InstaWP)

#### Subdomains that are considered as dev or staging: <a href="#subdomains_that_are_considered_as_dev_or_staging" id="subdomains_that_are_considered_as_dev_or_staging"></a>

* `local.*`
* `dev.*`
* `test.*`
* `stage.*`
* `staging.*`
* `stagingN.*` (SiteGround; `N` is an unsigned int)
* `*.wpengine.com` (WP Engine)
* `dev-*.pantheonsite.io` (Pantheon)
* `test-*.pantheonsite.io` (Pantheon)
* `staging-*.kinsta.com` (Kinsta)
* `staging-*.kinsta.cloud` (Kinsta)

Additionally, if your domain is `localhost` (with any port), it will also be treated as a localhost domain.

### Activation Scope on a Multi-Site Network

Kalium is compatible with multi-site networks, allowing you to use the theme across multiple sites within the same network. However, it’s important to note that each unique domain outside of the staging or development list is counted towards your activation limit. If your multi-site setup includes different domains, each one will require a separate license to comply with the activation scope.
