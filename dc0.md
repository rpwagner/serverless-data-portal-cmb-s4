---
title: "CMB-S4 Data Challenge 0"
author: "CMB-S4 Collaboration"
description: "CMB-S4 Data Challenge 0 (DC-0)"
date_created: "2023-03-16"
date_modified: "2023-09-08"
---

# Data Release: Data Challenge 0 (DC-0)

## Description

CMB-S4 Data Challenges involve the simulation, reduction, and analysis of a mock dataset corresponding to the current point design of the instruments and their observations and is used:

* to validate that the point design meets all of the project’s measurement and science requirements
* to verify that the project pipelines run sufficiently fast on that generation’s computational architecture(s), and scale sufficiently well to the CMB-S4 data volume.

DC-0 is the first execution of a Data Challenge run, it has been completed for Large Aperture Telescopes located in Chile (`CHLAT`) and the Small Aperture Telescopes located in the South Pole (`SPSAT`), the South Pole Large Aperture telescope (`SPLAT`) is still being worked on.

The full documentation of the release will be published publicly. For now, the best reference is the Technical Design to Measurement Requirements Appendix in the [`PBDR draft`](https://github.com/CMB-S4/PreliminaryBaselineDesignReport) in the Github repository, only accessible to members of the CMB-S4 Github organization.

## Data Access

Data access is currently restricted to members of the CMB-S4 Collaboration via a Globus Group.

See the [homepage of the data portal](index.md) for details on how to access and download the data.

## Data Products & Organization

The DC-0 data release includes a single Intensity and Polarization HEALPix map in FITS format for each split and for each frequency channel which includes:

* Galactic foregrounds
* Extragalactic foregrounds
* Cosmic Microwave Background signal
* Atmospheric and instrumental noise

and a second map which includes the map depth for Temperature and for Polarization.
More details about the data products are available in the map FITS headers and in the [Validation of the CMB-S4 Conceptual Design with Data Challenge 0 document (not available yet)]().

![depth map plot](images/cmbs4_dc0_map_depth.png)

Depth map for temperature for Chilean LAT in Equatorial coordinates.

Data splits are created by simulating each 1-hour long observation independently, then coadding all of them to create the full mission dataset `Split01` and coadding the observation in a round-robin fashion in 2, 4, 8, 16 and 32 independent maps. The full mission data set and 2-way splits are available here.

All other data products (including higher order data splits) are available on the CMB-S4 community filesystem at NERSC at `/global/cfs/cdirs/cmbs4/dc/dc0/mission/`.



## Datasets & Files

Files are grouped into datasets by telescope, time split, and frequency band. Each dataset is contained within a single folder and may contain subfolders. The top-level dataset folder contains a JSON file (`manifest.json`) using the BDBag [remote file manifest
format](https://github.com/fair-research/bdbag/blob/master/doc/config.md#remote-file-manifest) with the checksum, size, and HTTPS URL of each file.

The dataset pages provide a link to the dataset's folder in the Globus web app and links to the the invidual files for immediate download.


|                Link                | Telescope | Split | Frequency Band (GHz) | Number of Files | Total Size |
| ---------------------------------- | --------- | ----- | -------------------- | --------------- | ---------- |
| [Link](dc0-chlat-split01-025.html) | CHLAT     | `01`  | `025`                | `7`             | 17.3 GiB   |
| [Link](dc0-chlat-split01-040.html) | CHLAT     | `01`  | `040`                | `7`             | 17.3 GiB   |
| [Link](dc0-chlat-split01-090.html) | CHLAT     | `01`  | `090`                | `7`             | 17.3 GiB   |
| [Link](dc0-chlat-split01-150.html) | CHLAT     | `01`  | `150`                | `7`             | 17.3 GiB   |
| [Link](dc0-chlat-split01-230.html) | CHLAT     | `01`  | `230`                | `7`             | 17.3 GiB   |
| [Link](dc0-chlat-split01-280.html) | CHLAT     | `01`  | `280`                | `7`             | 17.3 GiB   |
| [Link](dc0-chlat-split02-025.html) | CHLAT     | `02`  | `025`                | `14`            | 34.5 GiB   |
| [Link](dc0-chlat-split02-040.html) | CHLAT     | `02`  | `040`                | `14`            | 34.5 GiB   |
| [Link](dc0-chlat-split02-090.html) | CHLAT     | `02`  | `090`                | `14`            | 34.5 GiB   |
| [Link](dc0-chlat-split02-150.html) | CHLAT     | `02`  | `150`                | `14`            | 34.5 GiB   |
| [Link](dc0-chlat-split02-230.html) | CHLAT     | `02`  | `230`                | `14`            | 34.5 GiB   |
| [Link](dc0-chlat-split02-280.html) | CHLAT     | `02`  | `280`                | `14`            | 34.5 GiB   |
| [Link](dc0-spsat-split01-025.html) | SPSAT     | `01`  | `025`                | `7`             | 276.1 MiB  |
| [Link](dc0-spsat-split01-040.html) | SPSAT     | `01`  | `040`                | `7`             | 276.1 MiB  |
| [Link](dc0-spsat-split01-085.html) | SPSAT     | `01`  | `085`                | `7`             | 276.1 MiB  |
| [Link](dc0-spsat-split01-095.html) | SPSAT     | `01`  | `095`                | `7`             | 276.1 MiB  |
| [Link](dc0-spsat-split01-145.html) | SPSAT     | `01`  | `145`                | `7`             | 276.1 MiB  |
| [Link](dc0-spsat-split01-155.html) | SPSAT     | `01`  | `155`                | `7`             | 276.1 MiB  |
| [Link](dc0-spsat-split01-230.html) | SPSAT     | `01`  | `230`                | `7`             | 276.1 MiB  |
| [Link](dc0-spsat-split01-280.html) | SPSAT     | `01`  | `280`                | `7`             | 276.1 MiB  |
| [Link](dc0-spsat-split02-025.html) | SPSAT     | `02`  | `025`                | `14`            | 552.1 MiB  |
| [Link](dc0-spsat-split02-040.html) | SPSAT     | `02`  | `040`                | `14`            | 552.1 MiB  |
| [Link](dc0-spsat-split02-085.html) | SPSAT     | `02`  | `085`                | `14`            | 552.1 MiB  |
| [Link](dc0-spsat-split02-095.html) | SPSAT     | `02`  | `095`                | `14`            | 552.1 MiB  |
| [Link](dc0-spsat-split02-145.html) | SPSAT     | `02`  | `145`                | `14`            | 552.1 MiB  |
| [Link](dc0-spsat-split02-155.html) | SPSAT     | `02`  | `155`                | `14`            | 552.1 MiB  |
| [Link](dc0-spsat-split02-230.html) | SPSAT     | `02`  | `230`                | `14`            | 552.1 MiB  |
| [Link](dc0-spsat-split02-280.html) | SPSAT     | `02`  | `280`                | `14`            | 552.1 MiB  |
