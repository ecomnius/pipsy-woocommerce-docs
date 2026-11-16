# Step 2 - Install Theme

After you download the package from ThemeForest, please unzip it. In the `Theme Files` folder you'll see a file called `pipsy.zip`, which is the main file needed to upload and install.

You can upload and install the theme with the **WordPress theme installer** or with **FTP**.

## Install via WordPress Dashboard

**Step 1** – Navigate to **Appearance > Themes**.

**Step 2** – Click the **Add New Theme** button on top of the page, then the **Upload Theme** button.

**Step 3** – Click **Choose File** and find the theme file you've just downloaded. If you downloaded the installable WordPress file, you don't need to unzip it. If you downloaded the full package, unzip the main ZIP first: inside it you will find `pipsy.zip`, which is the file you select to install.

**Step 4** - Click the **Install Now** button.

**Step 5** – When the upload and installation are complete, click **Activate**, or go to **Appearance > Themes** and activate the **Pipsy** theme.

## Install via FTP

If the WordPress installer fails, we recommend using FTP.

**Step 1** - Unzip `pipsy.zip`. You'll get a folder called `pipsy`.

**Step 2** - Use an FTP client like [FileZilla](https://filezilla-project.org/) and upload the extracted folder to the `wp-content/themes` folder on your host.

**Step 3** - Log in to your WordPress Dashboard, navigate to **Appearance > Themes** and click the **Activate** button of the **Pipsy** theme.

## Troubleshooting

1.  **"Are you sure you want to do this?"** or **"The link you followed has expired."** error

    It means your host limits the upload file size. Please install the theme via FTP, or contact your hosting company and ask them to increase the limit (see [Requirements for Pipsy](../getting-started/requirements-for-pipsy.md)).
2.  **The theme is missing the style.css stylesheet** error

    You have most likely uploaded the full package instead of the installable theme file. Unzip the package and upload `pipsy.zip` from its `Theme Files` folder.
