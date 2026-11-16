# Child Theme & Custom Code

Most changes don't need code: colors, fonts and radius are in [Theme Options](../theme-options/colors-and-typography.md), and layouts are edited in Elementor. When you do need custom CSS or PHP, put it where a theme update can't remove it.

{% hint style="danger" %}
Don't edit the files of the **Pipsy** theme directly. Every theme update replaces them.
{% endhint %}

## Custom CSS

For a few CSS rules, use one of these:

* **Theme Options > Advanced Settings > Custom CSS Code** – write the CSS without `<style>` tags.
* **Appearance > Customize > Additional CSS**.

Both are stored in the database and survive updates.

Pipsy exposes its design tokens as CSS variables with the `--nova-` prefix, set from Theme Options. Prefer changing the option to overriding the variable.

## Custom scripts

**Theme Options > Advanced Settings** has three fields for scripts such as analytics or chat widgets:

* **Custom Scripts Below `<head>`**
* **Custom Scripts just after opening `<body>`**
* **Custom Scripts on Footer before closing `</body>`**

## Child theme

Use a child theme to override template files or add PHP.

A child theme is included in the package: `Theme Files/pipsy-child.zip`. It holds a `style.css` for your CSS and a `functions.php` for your PHP, and it loads its stylesheet after the Pipsy theme CSS, so your rules win.

1. Install and activate the **Pipsy** theme first, see [Step 2 - Install Theme](../installation/step-2-install-theme.md).
2. Go to **Appearance > Themes > Add New Theme > Upload Theme**, choose `pipsy-child.zip` and click **Install Now**.
3. Click **Activate**. The parent theme must stay installed.

Add your CSS at the end of `pipsy-child/style.css` and your PHP in `pipsy-child/functions.php`. Pipsy updates do not overwrite these files.

{% hint style="info" %}
Theme Options and Elementor content are kept when you switch to the child theme. Menu locations and Customizer settings are stored per theme: check **Appearance > Menus > Manage Locations** after switching, and assign the menus again if a location is empty.
{% endhint %}

### Override a template

Copy the file from the parent theme to the same path in the child theme, then edit the copy. For example:

* `pipsy/woocommerce/content-product-default.php` → `pipsy-child/woocommerce/content-product-default.php` (the product card)
* `pipsy/woocommerce/order/tracking.php` → `pipsy-child/woocommerce/order/tracking.php` (the order tracking result)

After a theme update, compare your copies with the new parent files: **WooCommerce > Status** lists template overrides that are out of date.

## Hooks for developers

| Hook | Type | Use |
| --- | --- | --- |
| `novaworks/theme_styling` | Filter | The default colors, fonts, radius and palette behind Theme Options |
| `pipsy/metabox/meta_boxes` | Filter | The theme's meta boxes |
| `kitify/posts/metadata` | Filter | Meta types offered by the Kitify Posts widget |

The Pipsy widgets are registered by the **Pipsy Core** plugin. Put your own Elementor widgets in your own plugin or in the child theme, not in the folders of the parent theme or of Pipsy Core.
