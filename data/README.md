# Dataset P04 — Mangrove pesisir Kota Merauke 2005–2025

Dihasilkan oleh notebook (`P04_hasil.zip` → `07_dataset/`).

| Berkas | Isi |
|---|---|
| `P04_titik_label.csv` | Titik label: `idx` (indeks piksel grid), `kelas` (mangrove/daratan/air), `grp` (blok 2 km), `lon`, `lat` |
| `P04_sampel_latih.csv` | Fitur per titik per epoch 2005–2020: B, G, R, N, S1, S2, NDVI_p10/p50/p90, MNDWI, MVI, DEM; `y` (1 mangrove) |
| `P04_peta_mangrove.npz` | Peta mangrove `m2005`…`m2025` (1 mangrove, 0 bukan, 255 tidak ada data), grid 30 m UTM 54S (`X0`, `Y0` = pojok kiri atas) |
| `P04_peta_perubahan_2005_2025.npz` | `kelas`: 0 bukan mangrove stabil, 1 mangrove stabil, 2 hilang ke air, 3 hilang ke daratan, 4 bertambah dari air, 5 bertambah dari daratan, 255 tidak ada data |
| `P04_transek_mangrove.csv` | Per transek P01: lebar mangrove tiap epoch (m), fraksi depan mangrove, tipe depan 2005, LRR garis vegetasi dan air (dari P01) |

Transek dan LRR berasal dari dataset P01 (https://doi.org/10.5281/zenodo.24421128). Lisensi CC BY 4.0.

**EN.** Label points, training features, five-epoch mangrove maps, 2005–2025 change map and per-transect mangrove width linked to P01 erosion rates for the Merauke city coast. Licence CC BY 4.0.
