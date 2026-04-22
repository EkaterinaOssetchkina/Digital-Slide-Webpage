# Digital Slide Viewer — University of Toronto, Civil Engineering Materials Group

An open-source interactive viewer for petrographic thin section images, developed as part of ongoing research in construction materials at the University of Toronto.

**Live site:** http://individual.utoronto.ca/digital_slide/

![Digital Slide Webpage](/sample-images/digital-slide-webpage.png)

---

## Research context

This tool was developed alongside the publication:

> **Tapas de silice - a smorgasbord of reactive mineralogies and textures**
> Lucas Herzog Bromerchenkel, Oleksiy Chernoloz, Pengfei Zhao, Ekaterina Ossetchkina, and Karl Peterson
> *Journal of Microscopy*, 2022
> https://onlinelibrary.wiley.com/doi/full/10.1111/jmi.13059

The Veracruz Sand sample images included in this repository are the same specimens studied in the paper. The digital slide viewer was created as an educational and dissemination tool to allow readers to interactively explore the thin section images presented in the publication.

---

## Features

- **Filter switching** — toggle between PPL (plane-polarized light), XPL (cross-polarized light), and FLO (fluorescence) on each side of the viewer independently
- **Comparison slider** — drag the grey circle to reveal and compare two filters side by side
- **Pan** — click and drag the image to navigate across the thin section
- **Zoom** — use the slider below the image to zoom in and out; the image zooms in place around the centre
- **Calibrated scale bar** — a 1 mm scale bar updates automatically as you zoom
- **Upload your own images** — load your own PPL, XPL, and FLO images directly in the browser (no upload to server); images must be the same pixel dimensions

---

## Sample specimens

| Page | Specimen | Scale |
|------|----------|-------|
| Veracruz Sand | Veracruz siliceous sand (from Herzog Bromerchenkel et al. 2022) | 118 px/mm |
| Granite | Autumn Brown Granite (traditional cut stone) | 131 px/mm |
| Limestone | Wiarton Limestone (traditional cut stone) | 131 px/mm |
| Upload | User-supplied images | — |

---

## Customising the code

To repurpose this viewer for your own thin section images, replace the image URLs in the `#main` and `#overlay` CSS rules and update the button functions in the `<script>` block. Key lines to update:

- `background-image` in `#main` and `#overlay` — set your initial PPL and XPL images
- The `ppl()`, `xpl()`, `bw()`, `ppl_over()`, `xpl_over()`, `bw_over()` functions — point to your image files
- `scalebar` pixel/mm factor in `slider.oninput` and `reset()` — calibrate to your images

Alternatively, use the **Upload Your Own** page to load images directly without editing any code.

---

## Credits

**Group Lead:** Karl Peterson (karl.peterson@utoronto.ca)
**Developer:** Ekaterina (Katia) Ossetchkina (ekaterina.ossetchkina@mail.utoronto.ca)
University of Toronto — Civil Engineering Materials Group
