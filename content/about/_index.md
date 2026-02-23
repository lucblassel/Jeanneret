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
- Reference rendering from a BibTex file ([see below](#publications))
- Standalone pages 

## Publications 
{{ publications(path="/content/about/references.bib", show_preprints=true, show_only_preprints=false, sort_by_year=false) }}


