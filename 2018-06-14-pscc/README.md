# Slides for 2018-06-01 ARPA-E GRID DATA presentation

Pandoc converts the slideshow content in index.md into a reveal.js slideshow via the following command:

For local hosting:
```
pandoc -s -t revealjs --slide-level 1  -c pscc.css --bibliography bib.bib --csl ieee.csl -V revealjs-url=./revealjs index.md -o index.html
```

For pushing to website:
```
pandoc -s -t revealjs --slide-level 1 -c pscc.css --bibliography bib.bib --csl ieee.csl index.md -o index.html
```

- `-s` means "standalone", i.e. generate one HTML file with no dependencies.
- `-t revealjs` means convert to a reveal.js slideshow.
- `--slide-level 1` means treat level 1 headings (lines beginning with #) as separate slides. This circumvents Reveal's vertical slide capability, but for a 15-minute presentation it's best to use a horizontal layout anyway.
- `index.md` is the input Markdown file we want to convert
- `-o index.html` tells Pandoc to export our reveal.js HTML file with the name "index.html".

Reveal-specific configuration options are specified at the top of index.md (in YAML form):

- `pagetitle: Topological Graph Metrics`
- `controls: 'false'` turns off the garish animated arrows at lower right.
- `slideNumber: 'true'` turns on the much more useful slide numbers.
- `nocite: ...` specifies citations we want included on the references slide without citing them in any other slide.
