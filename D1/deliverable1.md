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

The goal of this report is to provide a summary of the current state of ice sheet and glacier delineation products, how they compare, and to provide recommendations for future steps.

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

A detailed examination of eight Greenlandic products (BedMachine, PROMICE, MAR, RACMO, ESA CCI, GIMP, Mouginot, and RGI v7 region 05) is shown below for six regions: Qaanaaq, Sisimiut, near the Geike Plateau, the southern tip of Greenland, central west Greenland near Daugaard-Jensen Gletsjer, and the west Greenlandic Kangerlussuaq fjord.

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

```{figure} fig/overlap_Geike.png
:alt: Map of overlapping masks in the Geike Plateau region, Greenland
:name: geike

Same display as {ref}`qaanaaq`, The Geike Plateau (southeast) shows one mask does not cover this area, as coverage drops from seven to six.
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

**Non-overlapping areas between masks on X axis and on Y axis in Greenland.** Scale (both number and color) is logarithmic. The diagonals are 0 because a product cannot be outside itself. An example interpretation of this graphic follows the RGI column (left column) starting at the bottom row. The bottom left square reports 10{math}`^{3.6}` km{math}`^2` (~4,000 km{math}`^2`) area of BedMachine ice shelf outside of the RGI peripheral glaciers. The third row up shows the 'harper_2023' peripheral glaciers have 10{math}`^{3.7}` km{math}`^2` (5,000 km{math}`^2`) outside of the RGI peripheral glaciers. Because this graphic is log scale, a change between two values of magnitude 1 represents ~10 % of the original values, and magnitude 2 (e.g. 10{math}`^5` to 10{math}`^3`) represents 1 %.

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

## Way forward

This is a draft / work in progress.

### Urgency and elements of context

The issue of double or undercounting is urgent: CMIP7 is underway, ISMIP7 is expected to release a simulation protocol soon (*when?*), IMBIE is a regularly recurring exercise with the next phase planned for (*when?*), and GlacierMIP4 is currently in preparation. **The primary and urgent aim of the working group should be to provide solutions to the double-counting problem for IPCC AR7 authors, as well as for all future publications and reports estimating sea-level rise and mass change from ice sheets and glaciers.**

Consultations by the working group have shown that the community is aware of the problem and that there is strong motivation to avoid double counting in future assessments. However, informal discussions have also revealed that the number of researchers working on global assessments is relatively small. For example, while ISMIP7 includes numerous working groups addressing different aspects of the protocol, the issue of defining the spatial domains of ice sheets and glaciers is often treated as a post-processing step that must be resolved centrally - not by the individual contributors.

It is important to note that **double counting becomes an issue primarily when attempting to combine results from different products or studies in global assessments**. If each individual study were internally consistent and transparent in defining its ice sheet and glacier domains, double counting could be avoided regardless of the definitions used. However, the problem arises when different studies use different domain definitions, or make no distinction at all, leading to inconsistencies and an inability to meaningfully compare results.

With this in mind, the working group should aim to:

- Provide a set of recommendations to the community, and to the IPCC authors, for how to avoid double counting in future assessments. These protocols should be tailored to and co-developed with collaborative efforts such as ISMIP, IMBIE, and others, in partnership with the working group.
- Provide datasets (i.e., recommended masks) to assist authors in avoiding double counting, or at least in clearly identifying and documenting the masks used in their assessments.
- Offer authoritative guidance, based on the support of both the working group and the broader community.

The timeframe is short, and the current position of the working group leads is that providing an entirely new, reviewed, and widely adopted mask in time for upcoming assessments is *not* feasible. It should not be the role of the working group to lead new mapping efforts (except potentially in cases of undercounting as discussed below) but the group can help motivate and coordinate such efforts. Furthermore, new products and outlines will emerge in the future anyways - the working group should rather work towards recommendations and protocols which are robust to the addition of new datasets in the future.

The following recommendations are based on the discussions and analyses above. The recommendations are not yet a consensus document, and we seek feedback from the working group and the community.

### General recommendations

Studies aiming to provide large-scale estimates of mass loss from glaciers and ice sheets should, where possible:

1. Provide aggregated estimates only when accompanied by a clear definition of the spatial domain used in the study.
2. Follow the FAIR principles of data discovery and accessibility, and include fine-grained information on the spatial domain, ideally enabling future global assessments to be reproduced or adapted using alternative domain definitions.
3. Exercise particular care when comparing results from previous studies, and remain aware of the importance of spatial domain definitions.
4. Use the products and masks recommended by the working group, and be mindful of the limitations of these products.

### Mountain glaciers

For historical and methodological reasons, glacier assessments have been performed almost exclusively using the RGI, thanks to strong community consensus around the RGI glacier outlines. While some recent observational and modeling efforts provide fine-grained estimates of glacier mass loss at the individual glacier level (e.g., @hugonnet_2021, @rounce_2023, @zekollari_2024), other studies provide estimates only at the regional level (e.g., @hock_2019, @marzeion_2020, @glambie_2025). The latter category complicates future accounting efforts if any changes are introduced in the RGI. If such changes are necessary, **they should be implemented as early as possible for future studies to take them into account**.

Regardless of the specific choices made for each ice sheet (see below), some RGI entities may ultimately be flagged as "belonging to the ice sheet". We suggest that a potential way forward for the RGI could be:

- RGI v7 outlines remain unchanged, as announced upon the dataset’s publication.
- Ice bodies newly tagged as "ice sheet" are flagged in RGI7 (and potentially retroactively in RGI6 as well) as an attribute, with no change to the outlines themselves.
- Future assessments are recommended to use this attribute when producing both aggregated and fine-grained results. For example, we could envision adding "subdomains" to RGI Region 05 (Greenland) and Region 19 (Antarctica), indicating which glaciers overlap with the new reference ice sheet mask, and should therefore be excluded from global glacier assessments.

With this approach, future studies will remain comparable to past assessments while also being compatible with fine-grained, domain-consistent global analyses in the future.

### Ice sheets

If the approach outlined above for the RGI is deemed reasonable, the remaining task for the working group is to agree on an "ice sheet mask" for both Greenland and Antarctica. The RGI can then be updated accordingly. There are some technical obstacles to this (for example, vector vs. raster formats) but these can be overcome.

The core challenge is therefore to identify the *best* or *most likely to be adopted* mask for both ice sheets. This is the hardest bit.

One radical—but elegant and clear—solution could be to define the ice sheets as "all land ice dynamically or geographically connected to the main ice sheet, including ice shelves". With this definition, a mask could be generated automatically using any raster dataset of ice cover (e.g., BedMachine), or through a spatial merge in a vector dataset.

Another approach could be to engage in a discussion (*how?*) and reach a decision (*how?*) on a suitable product—or perhaps arrive at a compromise between approaches.

We are starting this discussion below.

### Greenland

We could address the problem of double counting in Greenland through the following approaches using new and updated products.

#### Use upcoming GEUS dataset as baseline

In mid 2025 GEUS will be releasing an update to @citterio_2013 or a new outline of the conterminous Greenlandic ice sheet based on 2022 Sentinel imagery. We could recommend using this as a broader community definition of 'ice sheet'. RGI will update to exclude overlap, and become the definition of 'peripheral glaciers'. We will recommend that popular products such as BedMachine and RCMs update their domains, boundaries, or masks to match these two products to avoid double counting.

This plan does not address several important but separate issues raised by this working group, specifically:

- The connectivity of ice categorized as part of the GEUS ice sheet, including ice that appears visually connected in satellite imagery but may not be connected hydrologically, dynamically, or by other definitions.
- The lack of defined interior ice sheet basins, as existing basins (e.g., Zwally, Rignot, Mouginot) may not cover the entire ice sheet based on the new boundary.

These and other secondary issues will be addressed at a later stage.

#### Use BedMachine as baseline

BedMachine products have historically included an ice mask covering all of Greenland. This mask encompasses both glaciers and the ice sheet but does not currently distinguish between the two. While the mask is gridded, it is designed to be exhaustive and correct (errors or omissions in the outlines are expected to be corrected in future versions as they are discovered).

BedMachine could update its metadata and mask by implementing the ice sheet definition outlined above: distinguishing between contiguous ice (the “ice sheet”) and peripheral glaciers. The maintainers of BedMachine are reportedly open to this change (limited to adjustments in mask categories and metadata). For the RGI, this would effectively mean marking all glaciers loosely connected to the ice sheet as "ice sheet".

The main downside to this approach is that BedMachine is a raster product. If it becomes the reference, there must be strong community agreement that both glaciers and the ice sheet are accurately represented within it, and that there is no significant over- or under-counting of ice.

### Antarctica

Antarctica is an even more complicated environment. There is an equivalent to the GEUS 2022 Greendlandic outline found in @greene_2024 which provides annual masks, but these masks include but do not distinguish ice shelves.

The following recommendations come to mind. In the following, "RGI 19" and "RGI 20" refer to the masks of region 19 and 20 in the [RGI region files](https://www.glims.org/rgi_user_guide/02_regions_definition.html). Changes to these could imply altering the assignment of glacier outlines to these regions.

#### Use BedMachine as baseline

- Update BedMachine mask metadata (only metadata) to mark conterminous ice, ice shelves, and peripheral (unattached) ice.
- Update the outlines of the RGI 19 and RGI 20 glacier regions to match BedMachine conterminous and ice shelves
- Update RGI 19 region outlines to include all BedMachine peripheral and exclude the updated RGI 20 (BedMachine conterminous ice).
- Ideally, BedMachine peripheral is updated to match RGI 19 region outline, but prior discussion suggests this is not likely to happen, in which case  RGI 19 region outline is likely to be a superset of BedMachine peripheral.
- Recommend to community that they use the region masks definitions provided by RGI region files. The reason to recommend RGI and not BedMachine is that users of BedMachine may include peripheral ice, which would lead to double counting or under counting (if included in larger assessments that either include RGI 19, or assume that the Antarctica effort includes RGI 19).

#### Use @greene_2024 as baseline

- Select a @greene_2024 year, either 2000 (a very round number), 2020 (a recent round number) or 2022 (to match Greenland).
- Update @greene_2024 metadata to delineate ice shelves.
- Update RGI 20 region files to match the updated Greene product.
- Update RGI 19 region file to avoid overlapping with RGI 20, and to include any unattached ice not in the updated Greene product (perhaps using BedMachine unattached ice).
- Recommend to community that they use RGI 20 regions or the updated Greene product for main ice sheet, and add in RGI 19 if they want peripheral ice.

### Undercounting?

If undercounting occurs (e.g. there is ice that is not mapped anywher in any product), then a new mapping effort is necessary. By definition, it is not possible to quantify the amount of undercounting.

## Initial thoughts on the consequences of these recommendations

The proposed changes will likely affect the glacier and ice sheet communities differently.

The **ice sheet community** will have to update their masks to match the new standard, but this is a one-time effort for each sub-community (ISMIP for models, IMBIE for observations...) with very clear benefits. It must be added that despite of the benefits of having a unified definition of the ice sheet, neither ISMIP nor IMBIE have yet adopted a standard mask so far (ISMIP Greenland did). Our hope is that this WG could help in this regard. Initial discussions seem to indicate that both IMBIE and ISMIP are interested in adopting a standard mask, but there seems to be challenges too complex to be summarized here. Regardless, both IMBIE and ISIMIP should be responsible for enforcing the use of a standard mask in their respective efforts (e.g. during post-processing if required), regardless of this WG's recommendations.

For the **glacier community**, the changes as outlined above could mean that roughly ~80% of the glaciers in region 19 (Antarctic Periphery) and ~25% of the glaciers in region 05 (Greenland Periphery) could now be "part of the ice sheet" and eventually removed from RGI. This could have a significant impact on the future results of the glacier community, and could require a significant effort to update and communicate these results. This is mainly because in terms of relative area, the change is considerably larger for glaciers than it is for the ice sheets. Another reason is that the glacier community has been following the RGI standard for a long time, and results on e.g. sea-level rise contributions of glaciers in Antarctica and Greenland have been consistent over the years.

A strategy to communicate these changes to the public and community will be necessary. Fortunately, the changes could be done gradually. An ideal scenario could be:

1. IMBIE and ISMIP adopt the new standard mask for both ice sheets for their next assessments (ISMIP7, next iteration of IMBIE, etc.). Hopefully this should not change their results in a way imputable *only* to the adoption of the new mask, so that the change goes mostly unoticed (we could be wrong with this assessment).
2. Glaciers now classified as part of the ice sheet are flagged in the next RGI iteration (v7.2). These glaciers could either remain in the RGI files with a new attribute indicating their status or be removed, with a separate file provided for the removed outlines.
3. The glacier community is encouraged to produce results for the entire RGI but to communicate distinctions clearly. For example, global tables like those in Hugonnet et al. (2021) or Rounce et al. (2023) could include additional rows for the "previously glaciers, now ice-sheet" contributions from regions 05 and 19.
4. If the ice sheet community adopts a similar distinction (e.g., separating contiguous ice from "peripheral ice-sheet"), results from both communities could be compared, enhancing our understanding of methodological differences and allowing accross-community MIPs.
5. While changes to the RGI could occur within a year, the gradual communication of updated results may take considerably longer (e.g., RGI7 is still not widely adopted one year after publication).

Given the size of the respective communities and the historically strong community adoption of the RGI, changing RGI is still the scenario which is most likely to trigger the necessary change. Potential pushbacks that could arise are:

- The argument that peripheral glaciers behave like glaciers, so why don't the BedMachine or Greene products reflect this?
- Concerns that ice sheet models are less accurate for peripheral glaciers, potentially biasing results.

Personally, we (Ken & Fabien) believe these objections are valid but outweighed by the overarching goal of avoiding double counting in future IPCC reports and quantitative studies. We probably have missed many important aspects of the proposed change, and we are looking forward to the feedback from the community.
