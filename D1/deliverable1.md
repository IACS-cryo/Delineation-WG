---
numbering:
  code: false
  math: false
  headings: true
---

# Deliverable 1: Review report

**Authors:** Kenneth D. Mankoff<sup>1,2</sup>, Fabien Maussion<sup>3</sup>

**Affiliations:** <br>
<sup>1</sup>NASA Goddard Institute for Space Studies, New York, NY, 10025 USA <br>
<sup>2</sup>Autonomic Integra LLC, New York, NY, 10025 USA <br>
<sup>3</sup>School of Geographical Sciences, University of Bristol, Bristol, UK

**License:** CC-BY

**Executive Summary**

*In prep*

## Purpose and scope

Deliverable #1 of the International Association of Cryospheric Sciences (IACS) working group on the delineation of glaciers, ice sheets, and ice sheet basins aims to provide an overview of the current state of ice sheet and glacier delineation using several commonly used and widely cited products. These include datasets used by the glaciological community (e.g., BedMachine), observationally derived boundaries (e.g., RGI 7.0), and some regional climate model masks.

The goal of this report is to provide a summary of the current state of ice sheet and glacier delineation products.

## Data collection and methods

We reached out to the glaciological community ([CRYOLIST announcement](https://lists.cryolist.org/pipermail/cryolist/2022-November/008094.html)) and gathered a group of polar data experts, producers and users. We asked our members to provide information on their use of ice sheet and glacier masks and boundaries and collected the information as [GitHub Issues](https://github.com/IACS-cryo/Delineation-WG/issues?q=is%3Aissue%20label%3Ainfo%3Amask%20).

The following report is based on this initial consultation and contains new analyses of the presently available datasets. We provide an explanation of which products rely on which other products based on a community survey, and graphical statistical summaries showing the product union (X \union Y, i.e., area of overlap) and the product not-union (X \union Y’, i.e., area of product X outside of product Y). The regions highlighted in this report are illustrative examples of key issues and are not intended to be exhaustive or comprehensive.

## Products

We list all products either introducing or using a Greenland or Antarctic mask. A "mask" represents a gridded or vector file defining the spatial domain of a specific product.

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
| Mouginot (a.k.a IMBIE Greenland)                         | @mouginot_2019_data     | @mouginot_2019   |                                                       |          |

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
| Bedmap3                                                 | @pritchard_2025_data    | @pritchard_2025  |                                                       |                 |

## Results and discussion

The masks or boundaries themselves are rarely the primary focus of the work — exceptions include the RGI, @greene_2024, and a few others *(which ones?)*. For example, the BedMachine mask is a necessary input to perform the ice thickness inversion, while the MAR ice extent mask is required to accurately represent ice–atmosphere interactions and compute mass balance in MAR. The same is true for many of the other products mentioned above. Their primary focus is to provide a specific product (e.g., ice velocity, ice thickness, mass balance, etc.), with the mask being a secondary consideration.

For the products that are not mask producers but rather mask users, the choice of which mask to adopt appears to be based on reasonable and justifiable decisions. However, these decisions are often driven by ease of use, familiarity, or reliance on local or national datasets—rather than careful consideration of overlap (or lack thereof) with peripheral products such as the RGI, or the ease of comparison with downstream products.

### Greenland

Several Greenlandic products use the BedMachine mask (which is based on the GIMP mask) or the GIMP mask directly, which at its release may have been the most complete, accurate, and highest resolution mask. However, the GIMP mask is now based on a 10 year old paper (@howat_2014) and seven-year-old product (@howat_2017), and the mask itself uses data spanning 15 years, which is problematic considering the large annual changes in Greenland.

A detailed examination of eight Greenlandic products (BedMachine, PROMICE, MAR, RACMO, ESA CCI, GIMP, Mouginot, and RGI v7 region 05) is shown below for six regions: Qaanaaq, Sisimiut, near the Geikie Plateau, the southern tip of Greenland, central east Greenland near Daugaard-Jensen Gletsjer, and the east Greenlandic Kangerlussuaq fjord.

For all figures below, the RGI version used is v7.0. In this version, glacier outlines in Greenland correspond to connectivity level 0 and 1 in @rastner_2012 (level 2 - strongly connected - has been removed from the RGI with version 7).

```{figure} fig/overlap_Qaanaaq.png
:alt: Map of overlapping masks near Qaanaaq, Greenland
:name: qaanaaq

**Overlap map of eight masks (BedMachine, PROMICE, MAR, RACMO, ESA CCI, GIMP, Mouginot, and RGI v7 region 05) near Qaanaaq, Greenland.** The seven filled colors represent number of overlapping products when each is limited to the main (connected) ice sheet. The eight product is RGI v7 region 05 (peripheral Greenland, connectivity level 0 and 1) shown as a red outline. This graphic shows that some small areas that are in the RGI peripheral region are covered by two, three, or even seven of the other main ice sheet masks. Regions of the 'main ice sheet' are also defined differently among masks.
```

```{figure} fig/overlap_Sisimiut.png
:alt: Map of overlapping masks near Sisimiut, Greenland
:name: sisimiut

Same display as {ref}`qaanaaq`, but here showing a large area within in the RGI peripheral region that is covered by five of the other main ice sheet masks.
```

```{figure} fig/overlap_Geikie.png
:alt: Map of overlapping masks in the Geikie Plateau region, Greenland
:name: geikie

Same display as {ref}`qaanaaq`, The Geikie Plateau (southeast) shows one mask does not cover this area, as coverage drops from seven to six.
```

```{figure} fig/overlap_SouthGL.png
:alt: Map of overlapping masks near southern, Greenland
:name: southGL

Same display as {ref}`qaanaaq`, but here showing the southern tip of Greenland. Large areas covered by the RGI peripheral glacier product are also covered by main ice sheet mask products, and large areas not covered by RGI are only covered by some of the seven mask products.
```

```{figure} fig/overlap_daugaard.png
:alt: Map of overlapping masks near Daugaard-Jensen Gletsjer, West Greenland
:name: daugaard

Same display as {ref}`qaanaaq`, but here showing central west Greenland near Daugaard-Jensen Gletsjer.
```

```{figure} fig/overlap_Kangerlussuaq.png
:alt: Map of overlapping masks near Kangerlussuaq Fjord, West Greenland
:name: kangerlussuaq

Same display as {ref}`qaanaaq`, but here showing Kangerlussuaq Fjord, West Greenland.
```

The above figure provides a qualitative view of overlapping masks in a few regions of Greenland. The figures below show a quantitative display of more masks and what areas of each mask either overlaps the other masks, or is outside of the other masks.

```{figure} fig/set_union_GL.png
:alt: Map of overlapping masks, Greenland
:name: union_GL

**Overlapping areas between masks on X axis and on Y axis in Greenland.** Scale (both number and color) is logarithmic. The diagonal is the area of a product (100 % overlap with itself). An example interpretation of this graphic follows the RGI column (left column) starting at the bottom row. The bottom left square reports 10{math}`^{0.3}` km{math}`^2` (~2 km{math}`^2`) area overlap between RGI and areas flagged as "ice shelf" in BedMachine. The third row up shows overlap between RGI and peripheral glaciers in the 'harper_2023' product is 10{math}`^{4.8}` km{math}`^2` (~63096 km{math}`^2`). More interesting is overlap between RGI and the 'main@' rows, which are the primary ice sheet in those products. RACMO only overlaps RGI by 10{math}`^{3.4}` km{math}`^2` (~2,500 km{math}`^2`) but most other products overlap by ~10x as much (seen by the difference between ~10{math}`^3` and ~10{math}`^4`). The largest overlap is GIMP with 10{math}`^{4.4}` km{math}`^2` (~25,000 km{math}`^2`).

Data available [as a csv file](https://github.com/IACS-cryo/Delineation-WG/blob/main/D1/dat/sets_union_GL.csv).
```

An alternative view, rather than overlap, is area of product X outside of product Y. Because overlap is commutative (X overlap Y is the same as Y overlap X) the above figure is half empty. However, X not in Y is different than Y not in X, so the following figure contains twice as much information and occupies twice the area (same information density).

```{figure} fig/set_notin_GL.png
:alt: Map of not-in masks, Greenland
:name: notin_GL

**Non-overlapping areas between masks on X axis and on Y axis in Greenland.** Scale (both number and color) is logarithmic. The diagonals are 0 because a product cannot be outside itself. An example interpretation of this graphic follows the RGI column (left column) starting at the bottom row. The bottom left square reports 10{math}`^{3.6}` km{math}`^2` (~4,000 km{math}`^2`) area of BedMachine ice shelf outside of the RGI peripheral glaciers. The third row up shows the 'harper_2023' peripheral glaciers have 10{math}`^{3.7}` km{math}`^2` (5,000 km{math}`^2`) outside of the RGI peripheral glaciers. Because this graphic is log scale, a change between two values of magnitude 1 represents ~10 % of the original values, and magnitude 2 (e.g., 10{math}`^5` to 10{math}`^3`) represents 1 %.

Data available [as a csv file](https://github.com/IACS-cryo/Delineation-WG/blob/main/D1/dat/sets_notin_GL.csv).
```

### Antarctica

The state of masks in Antarctica is less homogeneous than in Greenland. The BedMachine mask uses unpublished data (see [GH Issue](https://github.com/IACS-cryo/Delineation-WG/issues/28)), and many products then use the BedMachine mask. However HIRHAM uses a 1994 USGS mask, and MetUM uses a mask from AVHRR data from the early 1990s.

An examination of seven Antarctica products (BedMachine, ESA CCI, Rignot (IMBIE), @greene_2022, NSIDC 0709, Bedmap3 and RGI region 19) is shown below for two regions: Wilkins ice shelf and Abbott ice shelf.

```{figure} fig/overlap_Wilkins.png
:alt: Map of overlapping masks near Wilkins ice shelf, Antarctica
:name: wilkins

**Overlap map of seven masks (BedMachine, ESA CCI, Rignot (IMBIE), @greene_2022, NSIDC 0709, Bedmap3, and RGI region 19) near Wilkins ice shelf, Antarctica.** The six filled colors represent number of overlapping products when each is limited to the main (connected) ice sheet. The seventh product is RGI region 19 (peripheral Antarctica) shown as a thin red outline. This graphic shows one product 'main ice sheet' includes the ice shelves and coastal islands.
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

**Overlapping areas between masks on X axis and on Y axis in Antarctica.** Scale (both number and color) is logarithmic. The diagonal is the area of a product (100 % overlap with itself). Of interest, the dark (low values) in the column over 'peripheral@RGI' shows overlap between RGI peripheral region and all other products. This overlap is sometimes small (~10{math}`^3` or 1000 km{math}`^2`), but sometimes 10 or 100 times as large (e.g., 10{math}`^5` km{math}`^2`).

Data available [as a csv file](https://github.com/IACS-cryo/Delineation-WG/blob/main/D1/dat/sets_union_AQ.csv).
```

An alternative view, rather than overlap, is area of product X outside of product Y. Because overlap is commutative (X overlap Y is the same as Y overlap X) the above figure is half empty. However, X not in Y is different than Y not in X, so the following figure contains twice as much information and occupies twice the area (same information density).

```{figure} fig/set_notin_AQ.png
:alt: Map of not-in masks, Antarctica
:name: notin_AQ

**Non-overlapping areas between masks on X axis and on Y axis in Antarctica.**

Data available [as a csv file](https://github.com/IACS-cryo/Delineation-WG/blob/main/D1/dat/sets_notin_AQ.csv).
```

## Summary

A community survey of existing ice masks and boundary products shows a wide range of products are used (as already documented in existing peer reviewed literature). The impact of the different masks are all quantified against each other in terms of area of overlap (union) and non-overlap (non-union). We note that reporting results in terms of area (e.g., km{math}`^2`) is a great measure of impact because the largest changes occur near the ice sheet edge, meaning small changes in area can have disproportionately large impact on change in mass balance. However, reporting results in area units is significantly easier, for a variety of reasons including that area is constant in time while mass flows vary through time, or that we may not have access to the model used with a given mask, and if existing models do not cover the entire mask, we cannot report mass balance for areas outside the model domain.
