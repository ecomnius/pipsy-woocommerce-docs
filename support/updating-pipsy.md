# Updating Pipsy

We release updates to fix bugs, add features and keep **Pipsy** compatible with new versions of WordPress, WooCommerce and Elementor. Every update is announced on the ThemeForest item page.

{% hint style="warning" %}
**Back up your site (files and database) before every update.** If you changed theme files directly, those changes will be lost. Put your customizations in a child theme so they survive updates, see [Child Theme & Custom Code](../customization/child-theme-and-custom-code.md).
{% endhint %}

Your content, Theme Options, menus and Elementor pages are stored in the database. Updating the theme doesn't change them.

## Update the theme

### Option 1 – Envato Market plugin (automatic)

1. Install the [Envato Market plugin](https://envato.com/market-plugin/).
2. Go to **Envato Market** in the WordPress admin and connect it with a token from your Envato account, as the plugin explains.
3. When a new version of Pipsy is available, it appears on the **Envato Market** page and in **Dashboard > Updates**. Click **Update**.

### Option 2 – Upload the new version (WordPress dashboard)

1. Download the latest **Installable WordPress file only** (`pipsy.zip`) from your ThemeForest **Downloads** tab.
2. Go to **Appearance > Themes > Add New Theme > Upload Theme** and choose `pipsy.zip`.
3. Click **Install Now**. WordPress tells you that the theme is already installed: click **Replace active with uploaded**.

### Option 3 – FTP

1. Download and unzip `pipsy.zip`.
2. Connect to your server and open `wp-content/themes/`.
3. Delete or rename the old `pipsy` folder, then upload the new `pipsy` folder.

## Update the bundled plugins

Kitify, Pipsy Core and Pipsy Package Demo Data are updated together with the theme.

1. After updating the theme, go to **Appearance > Install Plugins**. The menu item appears when a bundled plugin has a new version.
2. Plugins with a new version show **Update Required**. Select them, choose **Update** from the bulk action menu and click **Apply**.
3. If the download fails, update them by hand: go to **Plugins > Add New Plugin > Upload Plugin** and upload the ZIP files from the `plugins` folder of the full theme package. WordPress asks to **Replace current with uploaded**.

WooCommerce, Elementor and the other plugins from WordPress.org update from **Dashboard > Updates** as usual.

## After updating

1. Clear your caching plugin, server cache and CDN cache.
2. If WooCommerce asks to update its database or shows outdated template files, follow its notice in **WooCommerce > Status**.
3. In Elementor, go to **Elementor > Tools** and click **Regenerate Files & Data** if a page looks wrong.

{% hint style="info" %}
Don't run the demo importer again after an update. It is only meant for the first setup of a site.
{% endhint %}

## Changelog

Each release and its changes are listed in the changelog on the ThemeForest item page.

**Version 1.0.0** – Initial release.
