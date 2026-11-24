# Mangrove Change on the Merauke Coast 2005–2025 and Its Relation to Shoreline Erosion (P04)

Code, data and results for the study *"Mangrove Change on the Merauke Coast, Indonesia, 2005–2025 and Its Relation to Shoreline Erosion: Landsat Mapping with Labels from Global Map Agreement"*.

> **Ringkasan (ID):** Repositori ini berisi notebook, data, dan tabel hasil pemetaan mangrove pesisir Kota Merauke pada lima epoch (2005–2025) dari Landsat dengan Random Forest, menggunakan label dari kesepakatan Global Mangrove Watch v3 dan CGMD-Extent30 (tanpa survei lapangan), serta analisis hubungan lebar mangrove dengan laju abrasi pada transek P01. Semua tabel dan gambar tersedia dalam versi Indonesia (_ID) dan Inggris (_EN).

## Study design

| Item | Value |
|---|---|
| Study area | Merauke city coast (140.15–140.75° E, 8.30–8.80° S), coastal zone ≤ 20 m elevation, same grid as P01 |
| Epochs | 2005, 2010, 2015, 2020, 2025 (3-year Landsat 5/7/8/9 median composites) |
| Labels | Pixels on which all GMW v3 (2007–2020) and CGMD-Extent30 (2005–2023) maps agree: stable mangrove, land, water |
| Classifier | Random Forest (200 trees); features: 6 bands, NDVI p10/p50/p90, MNDWI, MVI, DEM |
| Validation | 5-fold spatial (2 km blocks); spatial + cross-epoch; agreement with GMW, CGMD, WorldCover |
| Change | Loss to water vs loss to other land; gain from water vs from land |
| Erosion link | P01 transects and vegetation-line LRR ([10.5281/zenodo.24421128](https://doi.org/10.5281/zenodo.24421128)); Mann-Whitney, Cliff's δ, Spearman, 2 km block bootstrap |

## Main results

| Item | Result |
|---|---|
| Validation on stable pixels | Accuracy 0.99 (spatial 5-fold); 0.986–0.992 cross-epoch |
| Agreement with CGMD (all coastal pixels) | F1 0.78–0.86 (GMW vs CGMD only 0.66) |
| Mapped mangrove area | 5,234.5 ha (2005) → 6,340.4 ha (2025); fluctuates 4,574–6,432 ha between epochs while CGMD stays 4,893–5,069 ha |
| Loss 2005–2025 | 806.2 ha, of which 24.9 ha (3.1%) to water and 781.3 ha (96.9%) to other land |
| Erosion, mangrove-fronted vs not (P01 transects) | Median LRR −0.56 vs −1.05 m/yr; significant erosion 51.6% vs 60.8% |
| Statistical support | Mann-Whitney p = 0.077; Cliff's δ 0.08 (95% block-bootstrap CI −0.16 to 0.32); difference driven by the km 28–32 accretion zone |

Per-epoch area fluctuations indicate that the per-epoch classification is not yet reliable for area-change accounting; see the manuscript limitations.

## Repository structure

```
notebooks/P04_notebook.ipynb   full pipeline (Google Colab + Earth Engine + scikit-learn)
data/                          label points, training sample, mangrove maps, change map, per-transect data
results/tables/                result tables and P04_hasil_ringkas.json
results/figures/               figures used in the manuscript
docs/diagrams/                 flowchart, context diagram, level-1 DFD (ID & EN)
```

## License

Code: MIT (`LICENSE`). Data, results and figures: CC BY 4.0.
