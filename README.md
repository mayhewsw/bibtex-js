bibtex-js
=========

## How to get BibTeX-js up and running.

Load javascript, add this to your html code:

```html
<script type="text/javascript" src="https://code.jquery.com/jquery-2.1.4.min.js"></script>
<script type="text/javascript" src="https://raw.githubusercontent.com/mayhewsw/bibtex-js/master/bibtex.js"></script>
```

Put bibtex input into a (hidden) textarea:

```html
<textarea id="bibtex_input" style="display:none;">
@book{book1,
  author = "Donald Knuth",
  title = "Concrete Mathematics"
}
</textarea>
```

Output will be displayed in the element with id "bibtex-display", add this to HTML:

```html
<div id="bibtex_display"></div>
```

That's it. Customize how publications are displayed using styles.

## How to style bibtex-js

The default style can be specified explicitly by adding the following to your html code:

```html
<div class="bibtex_template">
<div class="if author" style="font-weight: bold;">
  <span class="if year">
    <span class="year"></span>, 
  </span>
  <span class="author"></span>
  <span class="if url" style="margin-left: 20px">
    <a class="url" style="color:black; font-size:10px">(view online)</a>
  </span>
</div>
<div style="margin-left: 10px; margin-bottom:5px;">
  <span class="title"></span>
</div>
</div>
```

When class `if` is listed, the html element is only displayed if all fields listed as classes are present for an entry. Thus, the classes listed in `<span class="if url">` cause the url related elements to only be displayed if an entry has the `url` field. For all other elements, the contents is replaced by the field-name specified as its class.


## Credits
(c) 2010 Henrik Muehe.  MIT License

Exported to Github and updated by Stephen Mayhew