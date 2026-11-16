# Requirements for Pipsy

To use **Pipsy**, please make sure you are running a current version of WordPress, WooCommerce and Elementor. Please check the recommended server configuration for proper theme functioning:

**Minimum server configuration**

* WordPress version - 6.5 or higher
* PHP version - 7.4 or higher
* MySQL version - 5.7 or higher (or MariaDB 10.4 or higher)
* memory\_limit – 256M
* max\_execution\_time – 360
* max\_input\_time – 120
* upload\_max\_filesize – 64M

**Recommended server configuration**

* PHP version - 8.1 or higher
* MySQL version - 8.0 or higher (or MariaDB 10.6 or higher)
* memory\_limit – 512M
* max\_execution\_time – 480
* max\_input\_time – 240
* upload\_max\_filesize – 128M
* HTTPS enabled for the whole site

**Outgoing connections**

Your server must be able to make outgoing HTTPS requests to:

* `assets.novaworks.net` – to download Kitify, Pipsy Core and Pipsy Package Demo Data from **Appearance > Install Plugins**.
* `wordpress.org` – to download WooCommerce, Elementor and the other free plugins.
* `pipsy.ecomnius.com` – to download the demo images during the [demo import](../installation/step-5-import-demo.md).
* `fonts.googleapis.com` – to load the fonts you select in Theme Options.

{% hint style="warning" %}
Some plugins set their own PHP minimum. For example, recent versions of Contact Form 7 need a newer PHP version than the theme itself. If a plugin refuses to activate, check its requirements on WordPress.org and ask your host to upgrade PHP.
{% endhint %}
