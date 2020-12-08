# Presentations of Jonas Kersulis

Browser-based slideshows rendered with [reveal.js](https://revealjs.com).

I used to edit index.html files directly in a text editor. While [emmet](https://www.emmet.io/) made that somewhat doable, I was constantly distracted from my content by the need to match opening and closing tags, nest divs appropriately, etc. Then I discovered [how to use Pandoc to generate HTML slides](https://github.com/jgm/pandoc/wiki/Using-pandoc-to-produce-reveal.js-slides), and things got a lot easier. (See [this documentation also](http://pandoc.org/MANUAL.html#producing-slide-shows-with-pandoc).) Now I write each slideshow as a Markdown document, which itself becomes a concise version of the presentation content.

Note that presentations with citations require the Pandoc filter [pandoc-citeproc](https://github.com/jgm/pandoc-citeproc) to be available as an executable on the path.
