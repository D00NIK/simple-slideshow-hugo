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

1. Clone into `themes`

```bash
cd my-fun-site
git clone https://github.com/D00NIK/simple-slideshow-hugo themes/simple-slideshow-hugo
```

2. Add to `theme` in `hugo.toml` (or other extension)
```toml
theme = ['your-cool-theme', 'simple-slideshow-hugo']
```
