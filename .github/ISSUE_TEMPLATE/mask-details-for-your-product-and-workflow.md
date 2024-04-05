---
name: Mask details for your product and workflow
about: An issue template for entering details about your mask product and workflow
title: "[MASK]: <Entert product name here>"
labels: documentation, info:mask
assignees: ''

---

[Please enter text below, and fill in sentences where prompted. Remove text like this in brackets. Skip any questions that are not relevant for your product. Optionally select appropriate "labels" from the side-bar (e.g. greenland, antarctica, peripheral)]

# Overview

-   Product name and version: *PRODUCT NAME* [Example: RGI, GlacierMiP, BedMachine, ISMIP, or it could even be a study/paper in some cases]
-   Purpose of your product: [Example: mass balance, hydrology, ecological, etc.]
-   Geographic region: [Example: Greenland, Antarctica, Peripheral]


[Use the sections below to describe the upstream input mask for your work (if any), masks you generate internally (if any), and downstream output masks you release (if any), reasons for their usage, and cost of changing.]


# Upstream

[For each upstream mask product you used, copy and repeat this section. Or remove if no upstream mask]

-   What upstream mask product did you use? [Example: reference, DOI, or product name and version]

-   Reason for using this mask

-   If you modified the upstream mask, for example, to define and split ‘main’ vs. ‘peripheral’, how and why?

-   Effort required by you if upstream product changed (to a community standard)

-   If you used internal basins, which product and why?

-   If you subset to a geographical region (Greenland, Antarctica, sub-region, peripheral, individual glacier), how and why

-   Type: *vector, raster*

-   Resolution if raster:

-   Projection information: [Example: WKT string, proj4 string, EPSG code, or other]


# Internal

[Remove this section if no internal mask for your product]

-   All masks have boundaries. How, and why did you define yours?

-   If your product includes distinction between main and peripheral ice sheet, how did you define this? If possible, cite source, equation, pseudo-code, or text description)

-   Effort required if your internal product changed (to a community standard)

-   If you used internal basins, how did you define them, or which product and why?

-   Geographical region (Greenland, Antarctica, sub-region, peripheral, individual glacier)

-   Type: *vector, raster*

-   Resolution if raster:

-   Projection information: [Example: WKT string, proj4 string, EPSG code, or other]


# Downstream

Remove this section if no downstream output mask from your product

-   If your downstream output is different than internal, describe how and why.

# Other notes
