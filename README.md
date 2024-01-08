# Add Share buttons to Quarto HTML Documents

This extension allows to add buttons to share articles on various social media platforms.

## Installing

```sh
quarto install extension schochastics/quarto-social-share
```

This will install the extension under the `_extensions` subdirectory.
If you're using version control, you will want to check in this directory.

## Using

Add the following to the yaml header of your document.
You can set options to `false` if you don't want to display the respective share button.

```yaml
filters:
  - social-share
share:
  permalink: "https://mr.schochastics.net/"
  description: "awesome page"
  twitter: true
  facebook: true
  reddit: true
  stumble: true
  tumblr: true
  linkedin: true
  email: true
  mastodon: true
```

`permalink` is the url you are going to share and `description` and optional text.

the location of the buttons can so far only be placed after the html body, or
before the html body. To place it before the html body, add
```
location: "before-body"
```

to the share metadata.

The parameter `divclass` allows applying custom classes to the div containing
the share buttons

## Example

Here is the source code for a minimal example: [example.qmd](example.qmd)  
A rendered version can be found [here](https://schochastics.quarto.pub/social-share-buttons/).
