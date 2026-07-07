# JT TinyTools

**JT TinyTools** extends Joomla’s core TinyMCE editor with Bootstrap 5 content builders and privacy-friendly YouTube embeds.

It is designed for Joomla users who want to keep the default TinyMCE editor and improve the editing experience without depending on heavy third-party editors.

No JCE required.  
No additional CSS framework required.  
Uses Joomla’s default editor workflow and Bootstrap 5 classes.

---

## Features

JT TinyTools adds a **JT Tools** button to Joomla’s editor toolbar.

Available tools:

- Bootstrap 5 Alert builder
- Bootstrap 5 Button Link builder
- Bootstrap 5 Card builder
- Bootstrap 5 Columns builder
- Bootstrap 5 Accordion builder
- File Link builder
- YouTube no-cookie Embed builder

---

## Why JT TinyTools?

Joomla already includes TinyMCE as the core editor. JT TinyTools builds on that native editor instead of replacing it.

The goal is simple:

- Keep Joomla’s default editor
- Add practical content tools
- Use Bootstrap 5 classes already supported by Joomla templates
- Avoid unnecessary CSS frameworks
- Avoid iframe removal issues by using safe shortcode rendering
- Keep the workflow lightweight and Joomla-friendly

---

## Package structure

JT TinyTools is distributed as a Joomla package.

The package includes:

- `com_jttinytools`
- `plg_editors_xtd_jttinytools`
- `plg_content_jttinytools`

The package should be installed and updated as a single Joomla extension package.

---

## Requirements

- Joomla 6.x
- PHP 8.1+
- Joomla core TinyMCE editor
- A Joomla template that supports Bootstrap 5 classes

JT TinyTools does not load a custom CSS framework.  
Generated snippets use Joomla/template Bootstrap 5 classes.

---

## Installation

Download the latest package ZIP from GitHub Releases:

```text
pkg_jttinytools_0.4.3.zip
```

Install it from Joomla Administrator:

```text
System → Install → Extensions
```

After installation, open a Joomla article or content field that uses the core editor and click the **JT Tools** button.

---

## Usage

### Alert

Creates a Bootstrap 5 alert block.

Options include:

- Alert type
- Title
- Message
- Dismissible option

Example output:

```html
<div class="alert alert-info" role="alert">
  <h4 class="alert-heading">Alert title</h4>
  <p>Alert message</p>
</div>
```

---

### Button Link

Creates a Bootstrap 5 button link.

Options include:

- Button text
- URL
- Style
- Size
- Open in new tab

Example output:

```html
<a href="https://example.com" class="btn btn-primary" target="_blank" rel="noopener">
  Button text
</a>
```

---

### Card

Creates a Bootstrap 5 card block.

Options include:

- Title
- Text
- Optional button text
- Optional button URL

Example output:

```html
<div class="card mb-3">
  <div class="card-body">
    <h3 class="card-title">Card title</h3>
    <p class="card-text">Card text</p>
  </div>
</div>
```

---

### Columns

Creates a responsive Bootstrap grid layout.

Options include:

- Number of columns
- Breakpoint
- Gap
- Heading level

Example output:

```html
<div class="row g-3">
  <div class="col-md-6">
    <h3>Column 1</h3>
    <p>Column content.</p>
  </div>
  <div class="col-md-6">
    <h3>Column 2</h3>
    <p>Column content.</p>
  </div>
</div>
```

---

### Accordion

Creates a Bootstrap accordion block.

Options include:

- Number of items
- Heading prefix
- First item open/closed

---

### File Link

Creates a file or download link.

Options include:

- Link text
- File path or URL
- Text link or button style
- Button size
- Open in new tab
- Download attribute

Example output:

```html
<a href="images/sample.pdf" class="btn btn-primary" target="_blank" rel="noopener" download>
  Download file
</a>
```

The `download` attribute is useful for local files. Some browsers may ignore it for external URLs.

---

### YouTube no-cookie Embed

Creates a privacy-friendly YouTube embed.

Options include:

- YouTube URL or video ID
- Video title
- Ratio
- Privacy mode
- Lazy loading
- Optional “Open on YouTube” link

The YouTube builder inserts a safe shortcode into the editor instead of saving an iframe directly.

Example shortcode:

```html
{jttinytools-youtube id="PRinkGi0Hpk" title="YouTube video" ratio="16x9" privacy="1" lazy="1" link="0"}
```

The frontend output is rendered by the **Content - JT TinyTools** plugin using:

```text
youtube-nocookie.com
```

This avoids Joomla editor/text filter issues where iframe tags may be removed during save.

---

## Extension options

The editor button plugin includes options to enable or disable individual tools:

- Alert
- Button
- Card
- Columns
- Accordion
- File Link
- YouTube

Go to:

```text
System → Plugins → Button - JT TinyTools
```

or search for:

```text
JT TinyTools
```

---

## Content plugin

The content plugin is required for rendering YouTube shortcodes on the frontend.

Check that this plugin is enabled:

```text
System → Plugins → Content - JT TinyTools
```

If the content plugin is disabled, YouTube shortcodes will not be rendered on the frontend.

---

## Component

JT TinyTools also includes a small administrator component.

The component provides:

- Basic dashboard
- Extension status overview
- Joomla Options support
- Joomla Permissions support

Go to:

```text
Components → JT TinyTools
```

---

## Updates

JT TinyTools includes Joomla update server metadata.

Update XML:

```text
https://raw.githubusercontent.com/joomtheme/JT-TinyTools/main/updates/update.xml
```

Changelog XML:

```text
https://raw.githubusercontent.com/joomtheme/JT-TinyTools/main/updates/changelog.xml
```

---

## Package update behavior

JT TinyTools is distributed and updated as a Joomla package.

The component and plugins are child extensions of the package. Update and changelog metadata are provided at package level to avoid multiple separate update notices.

This is expected behavior.

---

## GitHub Release Asset

Use the package ZIP for installation:

```text
pkg_jttinytools_0.4.3.zip
```

Release download URL:

```text
https://github.com/joomtheme/JT-TinyTools/releases/download/v0.4.3/pkg_jttinytools_0.4.3.zip
```

---

## Support

Website:

```text
https://joomtheme.com
```

Support:

```text
support@joomtheme.com
```

---

## Author

**JoomTheme**

---

## License

GNU General Public License version 2 or later.

See:

```text
LICENSE.txt
```

---

## Current release

```text
0.4.3
```

---

## Status

JT TinyTools 0.4.3 is a stable MVP release prepared for Joomla Extension Directory testing.

It focuses on a clean Joomla core TinyMCE workflow, Bootstrap 5 content builders, and safe YouTube embed rendering.
