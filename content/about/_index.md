+++
title = "About the theme"
template = "standalone.html"
+++


[Jeanneret](/) is a simple, clean theme designed for personal academic websites. 
This theme is built for the [Zola](https://getzola.org) static website generator.

It features:
 1. A blogging section (just write your blogposts in the `content/posts/` directory). [see example post](@/posts/some-article.md)
 2. Standalone pages (e.g. for a course you are teaching), just use the `standalone.html` template.
 3. A homepage layout to present yourself. 

# Features

- Clean, readable typography and content layout
- Math rendering using [MathJax](https://www.mathjax.org/). Simply add `math=true` to the frontmatter of your post. 
- Reference rendering from a BibTex file ([see below](#rendering-bibtex))
- Standalone pages 

## Rendering BibTex 
The following bibliography is generated from the bibtex file shown below. It represents all the entries that this theme can deal with.  

{{ publications(path="/content/about/references.bib", show_preprints=true, show_only_preprints=false, sort_by_year=false) }}

<br> 
Bibtex content used to generate this bibliography
{{ raw_content(path="/content/about/references.bib", language="bibtex") }}

### Using the BibTex Capabilities
In practice this is achieved with macros defined in the [`bibmacros.html`](https://github.com/lucblassel/Jeanneret/blob/main/templates/macros/bibmacros.html) file.



For any entry in the bibtex file, you can add the `highlight_author={index}` in order to print the highlighted name in bold *(e.g. useful for listing your own publication)*. The index is 0-based, and invalid indices will result in no highlight being applied.

## Talks

You can also use the `talks(path=/path/to/datafile)` shortcode to render a list of presentations you have done. The file can be in one of the file formats parsed by the [Zola](https://www.getzola.org/documentation/templates/overview/#load-data)  *(i.e. `CSV`,`JSON`,`YAML` or `TOML`)*.  
Each entry must have a `title`, `date` and a `venue` field. Optionally you can also specify a `slides` field containing either the local path to the slides files or a remote URL. If your slides were build using beamer, you can also add an optional `source` field containing the path or remote link to your source files *(e.g. a repository, or a tarball)*. Finally, you can also specify the optional `comment` field to add any supplementary information. 


{{ talks(path="/content/about/talks.json") }}

