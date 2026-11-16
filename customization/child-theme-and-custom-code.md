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

<!-- TODO: no pipsy-child.zip exists in the repository yet. Add it to the ThemeForest package (as done for Formrest) and change this section to "install pipsy-child.zip from the package". -->

Create a folder `wp-content/themes/pipsy-child` with two files.

`style.css`:

```css
/*
Theme Name: Pipsy Child
Template: pipsy
Version: 1.0.0
Text Domain: pipsy-child
*/
```

`functions.php`:

```php
<?php
add_action( 'wp_enqueue_scripts', function () {
	wp_enqueue_style(
		'pipsy-child',
		get_stylesheet_uri(),
		array(),
		wp_get_theme()->get( 'Version' )
	);
}, 20 );
```

Then go to **Appearance > Themes** and activate **Pipsy Child**. The parent theme must stay installed.

{% hint style="info" %}
Theme Options, menus, widgets and Elementor content are kept when you switch to the child theme. Check **Appearance > Menus > Manage Locations** after switching, and assign the menus again if a location is empty.
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

Custom Elementor widgets belong in your own plugin or the child theme, not in the parent theme's folders.
