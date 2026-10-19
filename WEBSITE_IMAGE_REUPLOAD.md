# Oversized website photos retired (October 18, 2026)

This change removes all **39** static JPG/PNG/GIF images at least 1,000,000 bytes each (**147.65 MB**) from the current website branch. They remain recoverable in Git history. This is **website-hosted traffic**, not Supabase Storage egress.

The main homepage replaced **33** image elements: **23** with existing small WebP variants and **10** with the site logo until new photos are uploaded. The large Jasper hero background was replaced by a gradient on the homepage and Events page. The existing optimized product thumbnails remain intact, as does the manifest's original-source mapping for future reuploads. The thumbnail builder preserves existing variants when source files are absent.

## To restore photos

1. Resize your originals before uploading (typically 480–1200 pixels for website display), preferably WebP/JPEG, and target about 100–250 KB per normal card image.
2. Product photos: upload a smaller photo at the **same image path** shown below, then run the existing SEO/thumbnail build; its saved source mapping regenerates product WebP variants. Until then, existing variants remain visible.
3. Homepage photos without product variants: upload the smaller image, then change the matching element in `index.html` from `src="images/Logo.svg"` to the new file path shown in its `data-original-image` attribute.
4. For additional photo-gallery angles, restore the source image path and replace the placeholder `src` similarly; consider giving each reuploaded angle an optimized WebP filename.
5. No Supabase Storage originals were deleted or changed. Old files may temporarily remain in external CDN/browser caches.

## Removed source files

| Source path | Previous MB | Homepage replacement |
|---|---:|---|
| `images/cave gecko.jpg` | 21.15 | Not referenced by homepage image tags |
| `images/Hygrometer.jpg` | 12.39 | Optimized WebP |
| `images/Juvenile Pictus.jpg` | 8.06 | Not referenced by homepage image tags |
| `images/Mealworms.jpg` | 7.44 | Optimized WebP |
| `images/Jasper.JPG` | 6.00 | Gradient hero |
| `images/Superworms.jpg` | 5.93 | Optimized WebP |
| `images/Flat_Hide.JPG` | 5.18 | Not referenced by homepage image tags |
| `images/Pogostemon_Stellatus.jpg` | 4.59 | Optimized WebP |
| `images/Hornwort.jpg` | 4.50 | Optimized WebP |
| `images/Ludwigia_Repens.jpg` | 4.31 | Optimized WebP |
| `images/Dwarf Sword Grass.jpg` | 3.95 | Optimized WebP |
| `images/Coconut.jpg` | 3.62 | Placeholder |
| `images/mag ledge 4.jpg` | 3.40 | Placeholder |
| `images/mag ledge 2.jpg` | 3.22 | Placeholder |
| `images/mag ledge 3.jpg` | 3.17 | Placeholder |
| `images/Shadow-Box.jpg` | 3.04 | Optimized WebP |
| `images/mag ledge 1.jpg` | 3.02 | Optimized WebP |
| `images/sthenos.jpg` | 2.95 | Placeholder |
| `images/Box Hide.jpg` | 2.81 | Optimized WebP |
| `images/Metal Tong.jpg` | 2.81 | Optimized WebP |
| `images/Isopod_Vents.jpg` | 2.72 | Optimized WebP |
| `images/Floating-display.jpg` | 2.67 | Optimized WebP |
| `images/lugarti hide.jpg` | 2.48 | Optimized WebP |
| `images/Tex.jpg` | 2.28 | Placeholder |
| `images/Climbing_Vines.jpg` | 2.19 | Optimized WebP |
| `images/Potato.jpg` | 2.19 | Not referenced by homepage image tags |
| `images/Big mama.jpg` | 2.09 | Placeholder |
| `images/oreo crumble.jpg` | 1.99 | Optimized WebP |
| `images/Water_Dishes.jpg` | 1.88 | Optimized WebP |
| `images/Plastic tong2.jpg` | 1.80 | Placeholder |
| `images/rough greens.jpg` | 1.75 | Placeholder |
| `images/Food Ledge.jpg` | 1.67 | Optimized WebP |
| `images/Plastic tong1.jpg` | 1.62 | Optimized WebP |
| `images/Lil Susie.jpg` | 1.59 | Placeholder |
| `images/Lugarti Insectivore.jpg` | 1.51 | Optimized WebP |
| `images/Onyx.png` | 1.51 | Not referenced by homepage image tags |
| `images/Pollen.jpg` | 1.41 | Optimized WebP |
| `images/lugarti vitamin.jpg` | 1.41 | Optimized WebP |
| `images/lugarti water treatment.jpg` | 1.37 | Optimized WebP |
