# Themes for Signal Desktop Application

This repository contains pure CSS themes for the Signal Desktop application.

## Installation

Currently there is no automatic installation procedure. You have to manually edit
files. But don't worry, that's quite straightforward.

As with other Electron apps, Signal desktop app reads its resources from a file
named `app.asar`. You can access this file via
`C:\Users\user_name\AppData\Local\Programs\signal-desktop\resources\app.asar`. It's
in a format called "asar" which is a container format and can hold an entire
directory hierarchy of files (without compression). In order to install a theme,
we need to edit `/stylesheets/manifest.css` in `app.asar`.

Requirements:

* [7-Zip](https://www.7-zip.org/)
* [Asar7z plugin](https://www.tc4shell.com/en/7zip/asar/) for 7-Zip

With the Asar7z plugin installed, 7-Zip can easily read and modify asar files.
Installation steps:

1. Exit Signal if it's already running.
2. Open your `app.asar` file with 7-Zip.
3. Find `/stylesheets/manifest.css` in it. Right click on the CSS file and select Edit.
4. Copy the entire content of the theme you want to install and paste at the end of
   the `manifest.css`.
5. Save&close your editor and then 7-Zip will ask you if you want to apply
   modifications to the original asar file. Confirm it and then close 7-Zip.

It's done! Now you can open Signal and enjoy your new theme.

__Important Note:__ Every time you update Signal Desktop your customization will be
overwritten. So you've to reinstall the theme on every update.

## Bugs

Themes may be work in progress and also Signal updates can break them. You can
open issues on GitHub if you encounter bugs or you can fix them yourself and submit
pull request (highly appreciated).

## The Future

I hope Signal provides an official method in the future to let its users create
themes and install them directly in the application.

## LICENSE

See LICENSE file.
