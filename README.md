# hugo-module-google-fonts

A Hugo module for hosting Google Fonts on your site.

This Hugo Module was inspired by the Wordpress plugin OMGF.

## Installation

1. Initialize your Hugo site as a Hugo Module

   ```bash
   hugo mod init <repo_url>
   ```

2. Add this module to your Hugo site's configuration

    ```toml
    # hugo.toml
    [[module.imports]]
    path = "github.com/2b3d4f/hugo-module-google-fonts-local"
    ```

3. Add this to your site's configuration

    ```toml
    # hugo.toml
    [mediaTypes."font/woff2"]
    suffixes = [ "woff2" ]
    ```

This module only supports the `woff2` format.

## Examples

https://github.com/user-attachments/assets/e1344e4a-2f99-41ec-9d8b-1278f2557417

```gotmpl
{{- $url := "https://fonts.googleapis.com/css2?family=Noto+Emoji:wght@300..700&family=Roboto+Flex:opsz,wght@8..144,100..1000&display=swap" }}
{{- partialCached "gfonts.html" (dict "url" $url "fontsDir" "fonts" "cssDir" "css" "cssFile" "fonts.css" ) }}
```

### Variables

- `url` - the url to the Google Fonts CSS file
- `fontsDir` - the directory to store the fonts
- `cssDir` - the directory to store the CSS file
- `cssFile` - the name of the CSS file

## Settings

currently there are no settings available
