# Translation

Pipsy is translation ready. Its texts come from four places, and each is translated in its own way.

| Texts | Where they come from | How to translate |
| --- | --- | --- |
| Theme texts ("Add to bag", "Sizes %s", messages) | The **Pipsy** theme, text domain `pipsy` | Translation file, see below |
| Theme Options labels, Pipsy widgets (control labels and default texts), mega menu, product filter | The **Pipsy Core** plugin, text domain `pipsy-core` | Translation file, see below |
| Kitify widgets | The **Kitify** plugin, text domain `kitify` | Translation file |
| Page content, widget texts, menus | Your Elementor pages and templates | Edit them in Elementor, or use a multilingual plugin |

WooCommerce, Elementor and the other WordPress.org plugins download their own translations when you change the site language in **Settings > General > Site Language**.

## Translate the theme and Pipsy Core

The translation templates are included:

* Theme: `wp-content/themes/pipsy/languages/pipsy.pot`
* Pipsy Core: `wp-content/plugins/pipsy-core/languages/pipsy-core.pot`

### Option 1 – Loco Translate (in the dashboard)

1. Install and activate the free [Loco Translate](https://wordpress.org/plugins/loco-translate/) plugin.
2. Go to **Loco Translate > Themes > Pipsy** and click **New language**.
3. Choose your language. For the location, choose **Custom** (`wp-content/languages/loco/themes/`), so your translation is not lost when the theme is updated.
4. Translate the strings and click **Save**.
5. Repeat for **Loco Translate > Plugins > Pipsy Core**.

### Option 2 – Poedit (on your computer)

1. Open `pipsy.pot` in [Poedit](https://poedit.net/) and create a new translation for your language.
2. Save it as `pipsy-{locale}.po`, for example `pipsy-fr_FR.po`. Poedit also creates the `.mo` file.
3. Upload both files to `wp-content/languages/themes/`.
4. For Pipsy Core, save the files as `pipsy-core-{locale}.po` / `.mo` and upload them to `wp-content/languages/plugins/`.

Then set your language in **Settings > General > Site Language**.

## Translate widget texts

Every visible text of the Pipsy widgets is a control in the **Content** tab, with placeholders such as `{size}` for the dynamic parts. To translate a widget, edit its texts in Elementor. Keep the placeholders exactly as they are, including the curly brackets.

## Multilingual sites

Pipsy includes a `wpml-config.xml` file for [WPML](https://wpml.org/). For a store in several languages you need a multilingual plugin that supports WooCommerce and Elementor, such as WPML or Polylang.

{% hint style="warning" %}
Pipsy 1.0.0 has not been tested with WPML or Polylang. Try your multilingual plugin on a staging site first, and check the header, the mega menu, the Size Finder links and the Set Builder in each language.
{% endhint %}

## RTL languages

Pipsy 1.0.0 does not support right-to-left languages: the theme has no RTL stylesheet.
