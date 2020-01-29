# Markdown Images

This is a Sublime Text 3 plugin to render images inside of markdown files.

![Example](https://user-images.githubusercontent.com/1879136/73363560-ef6b0880-42e3-11ea-8b25-de885166a3b0.png)

## Usage

Images in markdown use the `![alt text](uri)` markup. Wherever this appears, this plugin can render the image specified by the URI below the line.

You can configure an image's dimensions by adding HTML `<img>` properties after the image markup: `![alt text](uri){width="200", height="200"}`. Everything between the `{}` will be copied to the `<img>` element that renders the image.

If the URI points to a file on disk, it is called a "local" image, and renders by default. If the URI points to an external (http, https, etc) resource, it is called a "remote" image, and does not render by default.

You can choose to show local, show remote or show all images from the [command palette](#commands) and with the [configuration](#configuration) settings.

## Configuration

By default, images are rendered when the file is first loaded. This can be configured with the `show_local_images_on_load` and `show_remote_images_on_load` settings.

Images can rendered on save with the `show_local_images_on_post_save` and `show_remote_images_on_post_save` settings.

Go to `Sublime Text -> Packages -> Package Settings -> MarkdownImages` (macOS menu) to edit your configuration.

Refer to the [default configuration file](./MarkdownImages.sublime-settings).

## Commands

* `markdown_images_show(show_local: bool, show_remote: bool)` - Show images from the local filesystem and/or remote URLs
* `markdown_images_hide()` - Removes all rendered images from the view

These can be activated with the command palette (`cmd+shift+p`):

* `MarkdownImages: Hide Images`
* `MarkdownImages: Show All Images`
* `MarkdownImages: Show Local Images`
* `MarkdownImages: Show Remote Images`

## Keybindings

This plugin adds no keybindings. You can set your own keybindings to the [commands](#commands).

## Notes

The URI portion of the `![alt text](uri)` markup must not contain spaces or else the markdown syntax parser (provided by other packages) will not recognize this as image markup.

Only PNG, JPG and GIF images are supported. 

SVG does not render inside of ST3 Phantom objects, unfortunately. 

Remote image loading runs in the main thread so it will stall ST3. Remote image loading is disabled

## Credits 

The image rendering code was seeded by [sublime_zk](https://github.com/renerocksai/sublime_zk)
