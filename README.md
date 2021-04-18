# tocmaker

`tocmaker` is a tool for importing and exporting pdf bookmark
with a custom format.


## Requirments

`tocmaker` utilizes [PDFtk](https://www.pdflabs.com/tools/pdftk-server/) to export and import pdf bookmarks.
They must be installed before running `tocmaker`.

## Custom format

This is a simple example of a bookmark file.

```
10 Chapter 1
25 Chapter 2
	26 Section 1
		26 SubSection 1
		27 SubSection 2
	30 Section 2
41 Chapter 3
```

## Example

### Export bookmarks

This will export the pdf bookmark into a file:

```shell
$ tocmaker export input.pdf -b bookmark.txt
```

### Override bookmarks

This will override the bookmarks of the pdf file:

```shell
$ tocmaker override input.pdf -b bookmark.txt
```

### Add bookmarks

This will add the bookmarks into a separate file:

```shell
$ tocmaker create input.pdf -b bookmark.txt -o out.pdf
```
