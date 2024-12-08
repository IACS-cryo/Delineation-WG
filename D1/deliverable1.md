# Deliverable 1: Review report

**Authors:** Kenneth D. Mankoff<sup>1,2</sup>, Fabien Maussion<sup>3</sup>

**Affiliations:** <br>
<sup>1</sup>NASA Goddard Institute for Space Studies, New York, NY, 10025 USA <br>
<sup>2</sup>Autonomic Integra LLC, New York, NY, 10025 USA <br>
<sup>3</sup>School of Geographical Sciences, University of Bristol, Bristol, UK

**License:** CC-BY

**Executive Summary**

The International Association of Cryospheric Sciences (IACS) working group on the delineation of glaciers, ice sheets and ice sheet basins deliverable #1 aims to provide an overview of the state of ice sheet delineations from some of the more common and popular products. These include basic data products used by much of the glaciological community (e.g., BedMachine), observational-derived boundaries (e.g., RGI 7.0) some regional climate model masks, etc.

We reached out to the glaciological community ([CRYOLIST announcement](https://lists.cryolist.org/pipermail/cryolist/2022-November/008094.html)) and gathered a group of polar data experts,  producers and users. We asked our members to provide information on... and add the information to github. The following report is based on this initial consultation and contains new analyses of the presently available datasets.

We provide an explanation for which products rely on which other products based on a community survey, and graphical statistical displays of the product union (X \union Y, or area overlap) and the product not-union (X \union Y', or area of product X outside of product Y).

## Products

We list all products either introducing or using a Greenland or Antarctic mask. A "mask" represents a gridded or vector files defining the spatial domain of a specific product.

This list is meant to be as exhaustive as possible. If a product is missing, please [reach out](https://github.com/IACS-cryo/Delineation-WG/issues).

### Greenland

<!-- Is it possible to configure Myst to accept links like gh:45 rather than the fulls URL? -->

| Name                                                     | Data citation           | Science citation | Details                                               | Comments |
|----------------------------------------------------------|-------------------------|------------------|-------------------------------------------------------|----------|
| MEaSUREs ITS_LIVE Greenland Monthly Ice Masks, Version 1 | @gardner_2023_data      | @greene_2024     | https://github.com/IACS-cryo/Delineation-WG/issues/45 |          |
| PISM                                                     |                         |                  | https://github.com/IACS-cryo/Delineation-WG/issues/43 |          |
| NORCE-CISM                                               |                         |                  | https://github.com/IACS-cryo/Delineation-WG/issues/41 |          |
| MAR                                                      |                         |                  | https://github.com/IACS-cryo/Delineation-WG/issues/39 |          |
| NHM-SMAP                                                 |                         |                  | https://github.com/IACS-cryo/Delineation-WG/issues/38 |          |
| ISSM                                                     |                         |                  | https://github.com/IACS-cryo/Delineation-WG/issues/36 |          |
| MetUM                                                    |                         |                  | https://github.com/IACS-cryo/Delineation-WG/issues/35 |          |
| GlacierMIP                                               |                         | @hock_2019       | https://github.com/IACS-cryo/Delineation-WG/issues/30 |          |
| RGI 7.0                                                  |                         |                  | https://github.com/IACS-cryo/Delineation-WG/issues/29 |          |
| BedMachine                                               | @NSIDC_BedMachine_GL_v5 | @morlighem_2017  | https://github.com/IACS-cryo/Delineation-WG/issues/27 |          |
| PROMICE                                                  | @citterio_2022          | @citterio_2013   |                                                       |          |
| ESA CCI                                                  |                         | @harper_2023     |                                                       |          |

### Antarctica

| Name                                                    | Data citation           | Science citation | Details                                               | Comments        |
|---------------------------------------------------------|-------------------------|------------------|-------------------------------------------------------|-----------------|
| MEaSUREs ITS_LIVE Antarctic Annual Ice Masks, Version 1 |                         | @greene_2022     |                                                       | Using only 2020 |
| PISM                                                    |                         |                  | https://github.com/IACS-cryo/Delineation-WG/issues/43 |                 |
| NORCE-CISM                                              |                         |                  | https://github.com/IACS-cryo/Delineation-WG/issues/41 |                 |
| MAR                                                     |                         |                  | https://github.com/IACS-cryo/Delineation-WG/issues/39 |                 |
| NHM-SMAP                                                |                         |                  | https://github.com/IACS-cryo/Delineation-WG/issues/38 |                 |
| ISSM                                                    |                         |                  | https://github.com/IACS-cryo/Delineation-WG/issues/37 |                 |
| MetUM                                                   |                         |                  | https://github.com/IACS-cryo/Delineation-WG/issues/35 |                 |
| HIRHAM5 Antarctic ice mask                              |                         |                  | https://github.com/IACS-cryo/Delineation-WG/issues/33 |                 |
| GlacierMIP                                              |                         | @hock_2019       | https://github.com/IACS-cryo/Delineation-WG/issues/30 |                 |
| RGI 7.0                                                 |                         |                  | https://github.com/IACS-cryo/Delineation-WG/issues/29 |                 |
| BedMachine                                              | @NSIDC_BedMachine_AQ_v3 | @morlighem_2019  | https://github.com/IACS-cryo/Delineation-WG/issues/28 |                 |

## Discussion

The masks or boundaries themselves are rarely the primary focus of the work (with the exception of RGI, @greene_2024, and a few others). For the remaining products that are not mask-producers but rather mask-users, the decision of which mask to begin with appears to be based on reasonable and justifiable decisions, but those decisions may be based on ease-of-use, familiarity, use of local or national products, etc. and not with significant consideration of overlap (or not) with peripheral products such as RGI, or ease-of-comparison with final downstream products.

### Greenland

Several Greenlandic products use the BedMachine mask (which is based on the GIMP mask) or the GIMP mask directly, which at its release may have been the most complete, accurate, and highest resolution mask. However, the GIMP mask is now based on a 10 year old paper (@howat_2014) and seven-year-old product (@howat_2017), and the mask itself uses data spanning 15 years, which is problematic considering the large annual changes in Greenland.

A detailed examination of seven Greenlandic products (BedMachine, PROMICE, MAR, RACMO, ESA CCI, GIMP, and RGI region 05) is shown below for four regions: Qaanaaq, Sisimiut, near the Geike Plateau, and the southern tip of Greenland.

```{figure} fig/overlap_Qaanaaq.png
:alt: Map of overlapping masks near Qaanaaq, Greenland
:name: qaanaaq

**Overlap map of seven masks (BedMachine, PROMICE, MAR, RACMO, ESA CCI, GIMP, and RGI region 05) near Qaanaaq, Greenland.** The six filled colors represent number of overlapping products when each is limited to the main (connected) ice sheet. The seventh product is RGI region 05 (peripheral Greenland, connectivity level 0 and 1) shown as a red outline. This graphic shows that some small areas that are in the RGI peripheral region are covered by two, three, or even five of the other main ice sheet masks. If the non-RGI masks include unattached glaciers, the number of overlap is even higher. Furthermore, regions of the 'main ice sheet' are defined differently in one mask (where overlap drops from six to five).
```

```{figure} fig/overlap_Sisimiut.png
:alt: Map of overlapping masks near Sisimiut, Greenland
:name: sisimiut

Same display as {ref}`qaanaaq`, but here showing a large area within in the RGI peripheral region that is covered by four of the other main ice sheet masks.
```

```{figure} fig/overlap_Geike.png
:alt: Map of overlapping masks near the Geike Plateau, Greenland
:name: geike

Same display as {ref}`qaanaaq`, but here showing only two small areas with overlap between RGI and two or three of the main ice sheet masks. The Geike Plateau (off figure to the southeast) shows one mask does not cover this area, as coverage drops from six to five.
```

```{figure} fig/overlap_SouthGL.png
:alt: Map of overlapping masks near southern, Greenland
:name: southGL

Same display as {ref}`qaanaaq`, but here showing the southern tip of Greenland. Large areas covered the RGI peripheral glacier product are also covered by three or four of the six mask products, and large areas not covered by RGI are only covered by three or five of the six mask products.
```

The above figure provides a qualitative view of overlapping masks in a few regions of Greenland. The figures below show a quantitative display of more masks and what areas of each mask either overlaps the other masks, or is outside of the other masks.


```{figure} fig/set_union_GL.png
:alt: Map of overlapping masks, Greenland
:name: union_GL

**Overlapping areas between masks on X axis and on Y axis in Greenland.** Scale (both number and color) is logarithmic. The diagonal is the area of a product (100 % overlap with itself). An example interpretation of this graphic follows the RGI column (first column) starting at the bottom row. The bottom left square reports 10{math}`^{0.3}` km{math}`^2` (~2 km{math}`^2`) area overlap between RGI and areas flagged as "ice shelf" in BedMachine. The second row shows overlap between RGI and peripheral glaciers in the 'harper_2023' product is 10{math}`^{4.8}` km{math}`^2` (~63096 km{math}`^2`). More interesting is overlap between RGI and the 'main@' rows, which are the primary ice sheet in those products. RACMO only overlaps RGI by 10{math}`^{3.4}` km{math}`^2` (~2,500 km{math}`^2`) but most other products overlap by ~10x as much (seen by the difference between ~10{math}`^3` and ~10{math}`^4`). The largest overlap is GIMP with 10{math}`^{4.4}` km{math}`^2` (~25,000 km{math}`^2`).

Data available [as a csv file](https://github.com/IACS-cryo/Delineation-WG/blob/main/D1/dat/sets_union_GL.csv).
```

An alternative view, rather than overlap, is area of product X outside of product Y. Because overlap is commutative (X overlap Y is the same as Y overlap X) the above figure is half empty. However, X not in Y is different than Y not in X, so the following figure contains twice as much information and occupies twice the area (same information density).

```{figure} fig/set_notin_GL.png
:alt: Map of not-in masks, Greenland
:name: notin_GL

**Non-overlapping areas between masks on X axis and on Y axis in Greenland.** Scale (both number and color) is logarithmic. The diagonals are 0 because a product cannot be outside itself. An example interpretation of this graphic follows the RGI column (first column) starting at the bottom row. The bottom left square reports 10{math}`^{3.6}` km{math}`^2` (~4,000 km{math}`^2`) area of BedMachine ice shelf outside of the RGI peripheral glaciers. The second row shows the 'harper_2023' peripheral glaciers have 10{math}`^{3.7}` km{math}`^2` (5,000 km{math}`^2`) outside of the RGI peripheral glaciers. Because this graphic is log scale, a change between two values of magnitude 1 represents ~10 % of the original values, and magnitude 2 (e.g. 10{math}`^5` to 10{math}`^3`) represents 1 %.

Data available [as a csv file](https://github.com/IACS-cryo/Delineation-WG/blob/main/D1/dat/sets_notin_GL.csv).
```

### Antarctica

The state of masks in Antarctica is less homogeneous than in Greenland. The BedMachine mask uses unpublished data (see https://github.com/IACS-cryo/Delineation-WG/issues/28), and many products then use the BedMachine mask. However HIRHAM uses a 1994 USGS mask, and MetUM uses a mask from AVHRR data from the early 1990s.

A detailed examination of six Antarctica products (BedMachine, ESA CCI, Rignot (IMBIE), @greene_2022, NSIDC 0709, and RGI region 19) is shown below for two regions: Wilkins ice shelf and Abbott ice shelf.

```{figure} fig/overlap_Wilkins.png
:alt: Map of overlapping masks near Wilkins ice shelf, Antarctica
:name: wilkins

**Overlap map of six masks (BedMachine, ESA CCI, Rignot (IMBIE), @greene_2022, NSIDC 0709, and RGI region 19) near Wilkins ice shelf, Antarctica.** The five filled colors represent number of overlapping products when each is limited to the main (connected) ice sheet. The sixth product is RGI region 19 (peripheral Antarctica) shown as a thin red outline. This graphic shows one product includes the ice shelves and coastal islands.
```


```{figure} fig/overlap_PIG.png
:alt: Map of overlapping masks near PIG, Antarctica
:name: PIG

Same display as {ref}`wilkins`, but near Abbott, Pine Island Glacier, and Thwaites ice shelves. This graphic shows a) general outline misalignment, and b) One product includes the ice shelves and coastal islands.
```

The above figure provide a qualitative view of overlapping masks in two regions of Antarctica. The figures below show a quantitative display of more masks and what areas of each mask either overlaps the other masks, or is outside of the other masks.

```{figure} fig/set_union_AQ.png
:alt: Map of overlapping masks, Antarctica
:name: union_AQ

**Overlapping areas between masks on X axis and on Y axis in Antarctica.** Scale (both number and color) is logarithmic. The diagonal is the area of a product (100 % overlap with itself). Of interest, the dark (low values) in the column over 'peripheral@RGI' shows overlap between RGI peripheral region and all other products. This overlap is sometimes small (~10{math}`^3` or 1000 km{math}`^2`), but sometimes 10 or 100 times as large (e.g. 10{math}`^5` km{math}`^2`).

Data available [as a csv file](https://github.com/IACS-cryo/Delineation-WG/blob/main/D1/dat/sets_union_AQ.csv).
```

An alternative view, rather than overlap, is area of product X outside of product Y. Because overlap is commutative (X overlap Y is the same as Y overlap X) the above figure is half empty. However, X not in Y is different than Y not in X, so the following figure contains twice as much information and occupies twice the area (same information density).

```{figure} fig/set_notin_AQ.png
:alt: Map of not-in masks, Antarctica
:name: notin_AQ

**Non-overlapping areas between masks on X axis and on Y axis in Antarctica.**

Data available [as a csv file](https://github.com/IACS-cryo/Delineation-WG/blob/main/D1/dat/sets_notin_AQ.csv).
```

<!--
# Old

This is the table from the proposal. We will likely want to include a modified version in D1.

| Name                             | Purpose                                               | Timespan                                        | Comments                                                                                                                | Data citation(s)                                                                   | Science citation          |
|----------------------------------|-------------------------------------------------------|-------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|---------------------------|
| BedMachine Greenland v5          | Bed topography                                        | 1993-2021                                       | Ice boundary is provided in mask but is not primary product                                                             | @NSIDC_BedMachine_GL_v5                                                            |                           |
| BedMachine Antarctica v3         | Bed topography                                        | 1970-2019                                       | Ice boundary is not primary product                                                                                     | @NSIDC_BedMachine_AQ_v3                                                            |                           |
| GEUS                             | Greenland boundary                                    | Nominal 1978-1987                               | Has “main”, “local”, and “disconnected”                                                                                 |                                                                                    | doi:10.5194/tc-7-445-2013 |
| GIMP                             | Land Ice/Ocean delineation                            | Two ice masks with nominal years 2000 and 2015. | Year 2000 ice mask compiled from data from 1999-2002 and 2015 ice mask compiled from data from the years 2013 and 2015. | <doi:10.5067/B8X58MQBFUPA>                                                         |                           |
| RGI                              | Outlines of glaciers outside of the ice sheets        | 2000 (deviations frequent)                      | Widely accepted standard, but overlaps with ice sheet products in this table                                            | <doi:10.7265/4m1f-gd79>                                                            |                           |
| “AutoTerm” Ice Masks             | Land Ice/Ocean delineation                            | 2018, 2019, 2020                                | The GIMP 2015 ice mask with termini from 295 (?) marine terming outlet glaciers grafted on for the years 2018-2020.     | <doi:10.5194/tc-17-3485-2023> Data not yet released by the NSIDC                   |                           |
| Greene 2022                      | Land Ice/Ocean delineation                            | 1997-2021                                       | 24 annual coastlines of Antarctica masked on a 240 m grid.                                                              | <doi:10.5281/zenodo.5903643>                                                       |                           |
| MEaSUREs Antarctic Boundaries v2 | Land Ice/Ocean delineation & Antarctic Basins         | IPY 2007-2009                                   | Maps of Antarctic ice shelves, basins and coastline from radar satellite data.                                          | https://nsidc.org/data/nsidc-0709/versions/2                                       |                           |
| MODIS Mosaic of Antarctica       | Land Ice/Ocean delineation                            | 2004, 2009, 2014                                | Antarctic coastline manually delineated, Methods defined in Scambos et al. (2007)                                       | <doi:10.5067/4ZL43A4619AF>; <doi:10.5067/RNF17BP824UM>; <doi:10.5067/68TBT0CGJSOJ> |                           |
| Radarsat Coastline               | Land Ice/Ocean delineation                            | 1997, 2000                                      | Antarctic coastline from Radarsat. Methods in Liu & Jezek (2004)                                                        | https://research.byrd.osu.edu/rsl/radarsat/data                                    |                           |
| Baumhoer 2021                    | Land Ice/Ocean delineation                            | 2018                                            | Antarctic coastline automatically extracted from Sentinel-1 imagery, 40 m resolution                                    | https://download.geoservice.dlr.de/icelines/ files                                 |                           |
| “Mouginot”                       | Glacier catchments/basins for the Greenland Ice Sheet | 2009-- (slow ice) & 2013-- (fast ice)           | Commonly used by community (e.g., IMBIE)                                                                                | <doi:10.7280/d1wt11>                                                               |                           |
| “Rignot Basins”                  | Antarctic & Greenland drainage systems                |                                                 | Commonly used by community (e.g., IMBIE)                                                                                | No DOI. http://imbie.org/imbie-3/drainage-basins                                   |                           |
| “Zwally Basins”                  | Antarctic & Greenland drainage systems                |                                                 | Commonly used by community (e.g., IMBIE)                                                                                | No DOI. Maybe http://imbie.org/imbie-3/drainage-basins                             |                           |
| Krieger 2023                     | Internal Greenlandic basins                           | TBD                                             | Methods defined in Krieger et al. (2020)                                                                                | In progress & unpublished                                                          |                           |

-->

## Way forward

With IPCC AR7 coming soon, we need to have something set-up soon. How?
