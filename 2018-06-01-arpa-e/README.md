# Slides for 2018-06-01 ARPA-E GRID DATA presentation

Pandoc converts the slideshow content in index.md into a reveal.js slideshow via the following command:

```
pandoc -s -t revealjs -c custom.css --slide-level 2 --mathjax -V theme=simple -V revealjs-url=http://lab.hakim.se/reveal-js index.md -o index.html
```

- `-s` means "standalone", i.e. generate one HTML file with no dependencies.
- `-t revealjs` means convert to a reveal.js slideshow.
- `-c custom.css` tells Pandoc to use the style rules in custom.css.
- `--slide-level 2` means treat level 2 headings (lines beginning with ##) as separate slides. This means level 1 headings are title slides that split the presentation into section.s
- `--mathjax`: I saw someone use this online. Without it, Pandoc gives me an error saying it's rendering my fenced clode blocks as TeX.
- `-V theme=simple` tells Pandoc to set a reveal.js-specific variable (`-V`) called `theme` to `simple`, which sets the presentation theme to simple. This seems to be the best choice for this presentation, as 'white' uses enormous fonts and the others have distracting colors.
- `-V revealjs-url=http://lab.hakim.se/reveal-js` tells Pandoc to use web-hosted reveal.js. If reveal.js is in the same directory locally, you can switch to `-V revealjs-url=./revealjs`.
- `index.md` is the input Markdown file we want to convert
- `-o index.html` tells Pandoc to export our reveal.js HTML file with the name "index.html".
