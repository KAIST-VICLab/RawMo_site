# RawMo project page

Source of the project page for **Back to Raw Motion: Latent-Free Diffusion Transformers for Text-to-Motion and Exact
Conditional Generation** (RawMo; Yun Chen, Jeonghyeok Do, Munchurl Kim; KAIST; arXiv preprint, 2026).

- Live page: https://kaist-viclab.github.io/RawMo_site/
- Code repository: https://github.com/KAIST-VICLab/RawMo

The page is plain HTML, CSS and JavaScript with no build step and no dependencies other than Google Fonts.
GitHub Pages serves it from the repository root (`.nojekyll` turns off Jekyll processing).

## Preview locally

Serve the folder over HTTP rather than opening `index.html` from disk, so that every path resolves as it does on GitHub Pages:

```bash
cd RawMo_site
python3 -m http.server 8000
# then open localhost:8000 in a browser
```

## Layout

```
index.html                the page: text-to-motion clips, the nine conditioning tasks, pelvis control, paper figures,
                          quantitative results, method overview and BibTeX
static/css/family.css     styles shared with the other KAIST-VICLab family pages (the same file on each)
static/js/family.js       scripts shared with those pages: navigation, abstract toggle, pending links, BibTeX copy,
                          image lightbox, tabs, table scroll cues
static/css/style.css      RawMo colours (top of the file), video cards, switchers, clip strips and table extras
static/js/main.js         video cards (loaded and played only when shown), task and example switchers, video lightbox
static/videos/            the demo clips: t2m/ (text-to-motion), cond/ (nine conditioning tasks), pelvis/ (pelvis
                          control); each <clip>.mp4 has a poster <clip>.jpg and a thumbnail <clip>_thumb.jpg
static/images/            paper figures: *_1200.jpg / *_2000.jpg are inline, *_full.jpg open in the lightbox;
                          og.jpg (social preview) and the logo files
static/paper/RawMo.pdf    the paper (PDF), opened by the Paper button and the navigation bar's Paper link
```

## Videos

The clips are cut from the authors' four demo videos (text-to-motion on HumanML3D and on KIT-ML, motion-conditioned
generation on HumanML3D, pelvis control on HumanML3D), one clip per example, at the source resolution and frame rate.
The titles, prompts, method names and errors in the clips are the authors'.

## Logo

`static/images/logo.svg` is the hero title: a wordmark in the face of the family pages, Outfit (outlined, so no font is
needed), with "Raw" in the page accent and "Mo" in the family ink `#1C2738`, next to the icon, a skeleton in motion.
`icon.svg` is the navigation and footer mark; `icon_square.svg` (the SVG favicon), `favicon-32.png`, `favicon-64.png`
and `apple-touch-icon.png` are the browser and home-screen icons. The colours follow the paper: `#46AAC5`, the colour
of RawMo in Fig. 1, is the logo colour; text, rules and borders use deeper shades of it (`#3BA0BB`, `#01758D`); highlighted
rows use `#E7F7F7`, the tint of the RawMo rows in the paper's tables. Orange marks given motion conditions and blue
generated motion, as in the paper's figures. All colours are set at the top of `static/css/style.css`.

## arXiv link

The paper was submitted to arXiv and its identifier is not known yet. Until it is, the arXiv button, the footer's arXiv
link and the BibTeX entry carry a placeholder identifier; such a link is shown as pending (the arXiv button carries a
"soon" badge) and does not navigate. Setting the identifier in `index.html` is enough; no CSS or JavaScript file needs
editing. The Paper button and the navigation bar's Paper link open the hosted PDF, `static/paper/RawMo.pdf`.
