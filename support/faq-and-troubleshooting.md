# FAQ & Troubleshooting

## Installation and demo import

**Do I need Elementor Pro?**

No. Pipsy works with the free version of Elementor. The Theme Builder (header, footer, shop, product and blog templates) comes from Kitify, which is included.

**Appearance > Install Plugins is missing.**

The menu item is only shown while a required or recommended plugin is missing, inactive or outdated. If all eight plugins are active, there is nothing to install.

**A bundled plugin can't be downloaded.**

Kitify, Pipsy Core and Pipsy Package Demo Data are downloaded from `assets.novaworks.net`. If your server blocks outgoing requests, upload the ZIP files from the `Plugins` folder of the theme package in **Plugins > Add New Plugin > Upload Plugin**.

**The demo import stops before the end.**

Increase `max_execution_time` and `memory_limit` (see [Requirements](../getting-started/requirements-for-pipsy.md)), then run it again from **Tools > Demo Importer**.

**Products and pages are imported without images.**

The images are downloaded from `pipsy.ecomnius.com` during the import. Ask your host to allow outgoing HTTPS requests, then click **Re-Import**.

**Can I use the demo images on my store?**

No. Demo images are for preview only and are not licensed for use on a live site.

## Design

**My pages look unstyled, or changes don't show.**

Go to **Elementor > Tools** and click **Regenerate Files & Data**. Then clear your caching plugin, your server cache and your CDN, and reload the page.

**The colors I set in Theme Options don't appear in a section.**

The section probably uses a fixed color instead of a Global Color. Edit the section in Elementor, open the color picker and choose the matching **Global Color**.

**How do I change the logo?**

Go to **Theme Options > Header > Site Header > Logo**, or select the Logo widget in the **Pipsy — Header** template. See [Theme Options](../theme-options/theme-options.md#logo).

**The header covers the top of my page.**

The page may have **Header over the first section** turned on. Edit the page with Elementor, open **Page Settings > Pipsy header** and set it to **Off**. See [Site Header](../layout/site-header.md#header-over-the-first-section).

**Changes in Theme Options > Header or Shop do nothing.**

Those options apply to the classic PHP templates. With the demo imported, the header, shop and product pages are Kitify templates: edit them in **Kitify > Theme Builder**.

## Shop

**The Size Finder shows nothing.**

No size has a height range yet. Go to **Products > Attributes > Size > Configure terms** and fill **Height from (cm)** and **Height to (cm)** on your sizes. See [Sizes & Size Finder](../woocommerce/sizes-and-size-finder.md).

**The Size Finder button opens an empty shop page.**

No product in stock uses that size. Check that your products use the same **Size** attribute (slug `size`) and have variations in stock.

**The Set Builder shows nothing, or skips a product.**

Each item must be a variable product with the Size attribute, published and in stock. Check the **Product ID** of each item. See [Pipsy Set Builder](../elementor/pipsy-set-builder.md).

**The set discount is not applied in the cart.**

The discount applies while every item of the set is in the cart, added with the widget's own button. Items added one by one from their product pages are not part of a set. Also check that **Set discount (%)** is above 0.

**The product page has no story section.**

The band is hidden until the product has content in **Product data > Editorial**. See [Product Story](../woocommerce/product-story.md).

**The filters don't show a size or a color.**

Empty terms are hidden. A term appears when at least one visible product in the current view uses it.

**The mega menu doesn't open.**

Check that **Enable Mega Menu** is on for the top level item, that you clicked **Save Changes** in the panel and **Save Menu**, and that the menu is assigned to **Main Navigation**. See [Menus & Mega Menu](../theme-options/menus-and-mega-menu.md).

## Forms

**The newsletter form shows an error.**

Add your MailChimp API key and list in **Kitify > Settings**.

**I don't receive messages from the contact form.**

Open **Contact > Contact Forms > Pipsy contact > Mail** and set your address in **To**. If mail still doesn't arrive, install an SMTP plugin; many hosts block PHP mail.

## Performance

* Use a caching plugin and, if you can, a CDN.
* Upload photos at the size you need (about 1100 px wide for product images) and in a modern format such as WebP.
* Keep only the plugins you use. Deactivate **Pipsy Package Demo Data** after the import.
* Select only the fonts and weights you need in **Theme Options > Typography**.

## Still stuck?

See [Support](support.md).
