# endless rain

Source for [endlessrain.xyz](https://endlessrain.xyz), a static site hosted on GitHub Pages. Plain HTML and CSS, no build step: whatever is on `main` is what's live.

## Layout

```
index.html            home page
blog.html             blog posts (newest first)
articles.html         list of articles
fiction.html          list of stories
moodboard.html
about.html
404.html              "page not found", also forwards old links to their new addresses

articles/             one file per article
fiction/              one file per story

assets/css/style.css  every page uses this one stylesheet
assets/icons/         favicons
favicon.ico           stays at the root because browsers look for it there

_templates/article.html   starting point for a new article or story (not published)
CNAME                 tells GitHub Pages to serve the site at endlessrain.xyz; don't delete
```

## Adding an article or story

1. Copy `_templates/article.html` into `articles/` or `fiction/`. Name it in lowercase with dashes, like `my-new-story.html`. No spaces in file names.
2. Update the title, description and links in the `<head>`, then put the text inside `<article>`, one `<p>` per paragraph.
3. Add an entry for it at the top of `articles.html` or `fiction.html`.

## Adding a blog post

Copy the `<article class="blog-post">` block in `blog.html`, paste it above the existing posts, and give it a new `id`, title and date.

## Changing the look

Colors, fonts and the reading width are variables at the top of `assets/css/style.css`.

## Previewing locally

Double-clicking an HTML file works. To see it exactly as it will behave online (including the 404 page), run this from the folder and open http://localhost:8000:

```
python3 -m http.server
```
