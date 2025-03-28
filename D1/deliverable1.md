# Deliverable 1: Review report

**Authors:** Kenneth D. Mankoff<sup>1,2</sup>, Fabien Maussion<sup>3</sup>

**Affiliations:** <br>
<sup>1</sup>NASA Goddard Institute for Space Studies, New York, NY, 10025 USA <br>
<sup>2</sup>Autonomic Integra LLC, New York, NY, 10025 USA <br>
<sup>3</sup>School of Geographical Sciences, University of Bristol, Bristol, UK

**License:** CC-BY

**Executive Summary**

The International Association of Cryospheric Sciences (IACS) working group on the delineation of glaciers, ice sheets and ice sheet basins deliverable #1 aims to provide an overview of the state of ice sheet delineations from some of the more common and popular products. These include basic data products used by much of the glaciological community (e.g., BedMachine), observational-derived boundaries (e.g., RGI 7.0) some regional climate model masks, etc.

We reached out to the glaciological community ([CRYOLIST announcement](https://lists.cryolist.org/pipermail/cryolist/2022-November/008094.html)) and gathered a group of polar data experts, producers and users. We asked our members to provide information on their use of ice sheet and glacier masks and boundaries and collecte the information as [GitHub Issues](https://github.com/IACS-cryo/Delineation-WG/issues?q=is%3Aissue%20label%3Ainfo%3Amask%20). The following report is based on this initial consultation and contains new analyses of the presently available datasets.

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
| Mouginot (a.k.a IMBIE Greenland)                          | @mouginot_2019_data     | @mouginot_2019   |                                                       |          |

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

A detailed examination of eight Greenlandic products (BedMachine, PROMICE, MAR, RACMO, ESA CCI, GIMP, Mouginot, and RGI region 05) is shown below for six regions: Qaanaaq, Sisimiut, near the Geike Plateau, the southern tip of Greenland, central west Greenland near Daugaard-Jensen Gletsjer, and the west Greenlandic Kangerlussuaq fjord.

```{figure} fig/overlap_Qaanaaq.png
:alt: Map of overlapping masks near Qaanaaq, Greenland
:name: qaanaaq

**Overlap map of eight masks (BedMachine, PROMICE, MAR, RACMO, ESA CCI, GIMP, Mouginot, and RGI region 05) near Qaanaaq, Greenland.** The seven filled colors represent number of overlapping products when each is limited to the main (connected) ice sheet. The eight product is RGI region 05 (peripheral Greenland, connectivity level 0 and 1) shown as a red outline. This graphic shows that some small areas that are in the RGI peripheral region are covered by two, three, or even seven of the other main ice sheet masks. Regions of the 'main ice sheet' are also defined differently among masks.
```

```{figure} fig/overlap_Sisimiut.png
:alt: Map of overlapping masks near Sisimiut, Greenland
:name: sisimiut

Same display as {ref}`qaanaaq`, but here showing a large area within in the RGI peripheral region that is covered by five of the other main ice sheet masks.
```

```{figure} fig/overlap_Geike.png
:alt: Map of overlapping masks near the Geike Plateau, Greenland
:name: geike

Same display as {ref}`qaanaaq`, The Geike Plateau (southeast) shows one mask does not cover this area, as coverage drops from seven to six.
```

```{figure} fig/overlap_SouthGL.png
:alt: Map of overlapping masks near southern, Greenland
:name: southGL

Same display as {ref}`qaanaaq`, but here showing the southern tip of Greenland. Large areas covered the RGI peripheral glacier product are also covered by main ice sheet mask products, and large areas not covered by RGI are only covered by some of the seven mask products.
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

## Way forward

The following are suggestions, and we seek feedback from working groups and team members. **This is not yet a consensus document, nor a plan to be implemented**. This section will be published on-line and then linked to a GitHub discussion, then a final edit based on feedback in the discussion.

### Greenland

We can address the problem of double counting in Greenland through the following approach using new and updated products.

In mid 2025 GEUS will be releasing an update to @citterio_2013 or a new outline of the conterminous Greenlandic ice sheet based on 2022 Sentinel imagery. We recommend using this as a broader community definition of 'ice sheet'. RGI will update to exclude overlap, and become the definition of 'peripheral glaciers'. We will recommend that popular products such as BedMachine and RCMs update their domains, boundaries, or masks to match these two products to avoid double counting.

This plan does not address several important but separate issues raised by this working group, specifically:

- The connectivity of ice categorized as part of the GEUS ice sheet, including ice that appears visually connected in satellite imagery but may not be connected hydrologically, dynamically, or by other definitions.
- The lack of defined interior ice sheet basins, as existing basins (e.g., Zwally, Rignot, Mouginot) may not cover the entire ice sheet based on the new boundary.

These and other secondary issues will be addressed at a later stage.

### Antarctica

Antarctica is a more complicated environment. There is an equivalent to the GEUS 2022 Greendlandic outline found in @greene_2024 which provides annual masks, but these masks include but do not distinguish ice shelves.

The following recommendations come to mind. In the following, "RGI 19" and "RGI 20" refer to the masks of region 19 and 20 in the [RGI region files](https://www.glims.org/rgi_user_guide/02_regions_definition.html). Changes to these would imply altering the assignment of glacier outlines to these regions.

#### Use BedMachine as baseline

- Update BedMachine mask metadata (only metadata) to mark conterminous ice, ice shelves, and peripheral (unattached) ice.
- Update the outlines of the RGI 19 and RGI 20 glacier regions to match BedMachine conterminous and ice shelves
- Update RGI 19 region outlines to include all BedMachine peripheral and exclude the updated RGI 20 (BedMachine conterminous ice).
- Ideally, BedMachine peripheral is updated to match RGI 19 region outline, but prior discussion suggests this is not likely to happen, in which case  RGI 19 region outline is likely to be a superset of BedMachine peripheral.
- Recommend to community that they use the region masks definitions provided by RGI region files. The reason to recommend RGI and not BedMachine is that users of BedMachine may include peripheral ice, which would lead to doule counting or under counting (if included in larger assessments that either include RGI 19, or assume that the Antarctica effort includes RGI 19).

#### Use @greene_2024 as baseline

- Select a @greene_2024 year, either 2000 (a very round number), 2020 (a recent round number) or 2022 (to match Greenland).
- Update @greene_2024 metadata to delineate ice shelves.
- Update RGI 20 region files to match the updated Greene product.
- Update RGI 19 region file to avoid overlapping with RGI 20, and to include any unattached ice not in the updated Greene product (perhaps using BedMachine unattached ice).
- Recommend to community that they use RGI 20 regions or the updated Greene product for main ice sheet, and add in RGI 19 if they want peripheral ice.

### Initial thoughts on the consequences of these recommendations

The proposed changes will likely affect the glacier and ice sheet communities differently.

The **ice sheet community** will have to update their masks to match the new standard, but this is a one-time effort for each sub-community (ISMIP for models, IMBIE for observations...) with very clear benefits. It must be added that despite of the benefits of having a unified definition of the ice sheet, neither ISMIP nor IMBIE have yet adopted a standard mask so far. Our hope is that this WG would help in this regard. Initial discussions seem to indicate that both IMBIE and ISMIP are interested in adopting a standard mask, but there seems to be challenges too complex to be summarized here. Regardless, both IMBIE and ISIMIP should be responsible for enforcing the use of a standard mask in their respective efforts (e.g. during post-processing if required), regardless of this WG's recommendations.

For the **glacier community**, the changes as outlined above would mean that roughly ~80% of the glaciers in region 19 (Antarctic Periphery) and ~25% of the glaciers in region 05 (Greenland Periphery) would now be "part of the ice sheet" and eventually removed from RGI. This would have a significant impact on the future results of the glacier community, and would require a significant effort to update and communicate these results. This is mainly because in terms of relative area, the change is considerably larger for glaciers than it is for the ice sheets. Another reason is that the glacier community has been following the RGI standard for a long time, and results on e.g. sea-level rise contributions of glaciers in Antarctica and Greenland have been consistent over the years.

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
