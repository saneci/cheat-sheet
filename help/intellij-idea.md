# IntelliJ IDEA cheat sheet

## Table of content

1. [Automatic Javadoc rendering](#automatic-javadoc-rendering)
2. [Bypass plugin installation blocking](#bypass-plugin-installation-blocking)

## Automatic Javadoc rendering

1. Open **Settings | Editor | General | Appearance**
2. Enable the **Render Documentation Comments** checkbox
3. Now the documentation comments in the code are automatically rendered

## Bypass plugin installation blocking

There is a working way to download a plugin bypassing the check:

1. Open the plugin page in the marketplace
2. Go to the **Versions** tab and choose a version
3. Start the download - the browser will redirect you to a link like `https://plugins.jetbrains.com/files/...`
4. Replace the `plugins.jetbrains.com` domain with `downloads.marketplace.jetbrains.com`
5. The file will be downloaded directly from the CDN

Alternatively, use the **RuJet installer** browser extension for Chrome/Firefox - it performs this replacement
automatically.
