# simple-slideshow-hugo
Pros:
- Clean, efficient code
- Not using any JS framework, library and other bloat
- Lazy loading
- Easy set-up

Cons:
- Basic design
- Not much configuration (unless you won't touch code, but you **should**)
- One per page since I didn't use any uid's for classes and js

## Usage

1. Clone into `themes`:

```bash
cd my-fun-site
git clone https://github.com/D00NIK/simple-slideshow-hugo themes/simple-slideshow-hugo
```

2. Add to `theme` in `hugo.toml` (or other extension):
   
```toml
theme = ['your-cool-theme', 'simple-slideshow-hugo']
```

3. Use as [shortcode](https://gohugo.io/content-management/shortcodes/) in content:

```md
{{< simple-slideshow >}}
```

Note that it's intended to be used in [leaf bundles](https://gohugo.io/content-management/page-bundles/#leaf-bundles). Two examples below:

```
content/
├── posts
│   ├── my-first-post
│   │   ├── image1.jpg
│   │   ├── image2.png
│   │   └── index.md        --> use shortcode here
│   ├── my-second-post
│   │   ├── img
│   │   │   ├── image1.jpg
│   │   │   └── image2.png
│   │   └── index.md        --> or like here
```

## Configuration

- `dir` - default: `/` - change where the shortcode looks for images
- `topSlideBar` - default: `true` - slidebar for thumbnails on top
- `scrollIntoView` - default: `true` - when changing slide scrolls if the image is outside of user's vision
- `maxThumbnailHeight` - default: 150 - max thumbnail height in px.

Example:

```md
{{< simple-slideshow dir=img/* topSlideBar=false scrollIntoView=false maxThumbnailHeight=300 >}}
```

## TO DO

