# FileMaker Markdown Addon

This addon allows you to display markdown data as HTML within a FileMaker web viewer. It supports custom CSS styling through a `css` attribute and markdown content through a `markdown` attribute.

## Features

- Render markdown content as HTML.
- Apply custom CSS styles via a URL link.

## Installation

To install, download or clone this repository and double-click on the `Markdown.fmaddon` file. Alternatively, you can use the `Markdown Example` and get the dist code to use it on your own.

## Usage

To use the addon, you need to provide JSON properties to the `WebComponents.GetCode` function. Below is an example of how to set the markdown and optional CSS attributes:

```
WebComponents.GetCode ( "markdown" ; 
   JSONSetElement ( "{}" ; 
      ["markdown" ; "#Heading 1" ; 1];
      ["css" ; "https://unpkg.com/bamboo.css" ; 1]
   ) ; 
   False 
)
```

### Attributes

- `markdown`: The markdown text to be rendered as HTML.
- `css`: (Optional) A URL link to a CSS file for custom styling.

## Example

```
WebComponents.GetCode ( "markdown" ; 
   JSONSetElement ( "{}" ; 
      ["markdown" ; "# Welcome to FileMaker Markdown Addon" ; 1];
      ["css" ; "https://unpkg.com/bamboo.css" ; 1]
   ) ; 
   False 
)
```

This example will render a heading with the text "Welcome to FileMaker Markdown Addon" and apply styles from the Bamboo CSS framework.

## License

This project is licensed under the MIT License.