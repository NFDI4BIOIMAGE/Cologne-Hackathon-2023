# 👋 Cologne-Hackathon-2023

[![License: CC BY 4.0](https://img.shields.io/badge/License-CC_BY_4.0-lightgrey.svg)](https://creativecommons.org/licenses/by/4.0/)  

This is the repository for documentation during the first **NFDI4Bioimage - TA3-Hackathon - UoC-2023** (in short: **Cologne Hackathon**).  


**TOC - In this README:**  
- [👋 Cologne-Hackathon-2023](#-cologne-hackathon-2023)
  - [Context of proposed topics](#context-of-proposed-topics)
  - [Brief report about the event](#brief-report-about-the-event)
    - [Setting the Stage](#setting-the-stage)
    - [Potential topics](#potential-topics)
    - [Spot on the Topics](#spot-on-the-topics)
    - [Let the show(s) begin](#let-the-shows-begin)
      - [Workflow and roadmap session(s)](#workflow-and-roadmap-sessions)
      - [Topic selection on-site](#topic-selection-on-site)
    - [Hacking - Documentation](#hacking---documentation)
    - [Use Cases](#use-cases)
    - [Shine!](#shine)
    - [42?](#42)
    - [Closing the Hackathon](#closing-the-hackathon)
  - [Overview of the content in this repository](#overview-of-the-content-in-this-repository)
  - [Contributions](#contributions)
    - [Contributors in alphabetical order](#contributors-in-alphabetical-order)
  - [Zenodo submission](#zenodo-submission)
  - [Organizers](#organizers)
  - [Acknowledgement](#acknowledgement)
  - [Funding - for this hackathon](#funding---for-this-hackathon)
    - [NFDI4Bioimage](#nfdi4bioimage)
    - [Other Organisations](#other-organisations)
      - [CEPLAS](#ceplas)
      - [CECAD](#cecad)
      - [CRC TRR341](#crc-trr341)


## Context of proposed topics

Open Microscopy Environment Remote Objects ([**OMERO**](https://doi.org/10.1038/nmeth.1896)) is a data management platform used in experimental biology and is in particular specialized for the needs of imaging data.  

Imaging data can be very complex. An image acquisition usually comprises multiple files of different types covering the data, and respective metadata in one directory or condensed to one object in a vendor-specific file format. If not managed accordingly in an Research Data Management (RDM) compliant way, this can cause all kinds of problems for downstream analysis, linking it with data across disciplines and preventing tools from being interoperable. [**OME-Zarr**](https://doi.org/10.1007/s00418-023-02209-1) is one such format which tries to avoid such obstacles and minimize data loss upon conversion.  

OMERO supports with handling this specific type of data. It extracts, maps and stores metadata in a relational database and enriches it with proprietary-file-format-specific metadata if required while converting the proprietary file formats using [Bio-Formats](https://doi.org/10.1083/jcb.201004104).  

Moreover, using OMERO, researchers can visualize, analyze and process their imaging data. One example is a volume viewer (VolViewer). However, other solutions for more specific 3D volume visualization accessible from OMERO are desired. Two options for this are [**3D-Slicer**](https://www.slicer.org/) and [**neuroglancer**](https://doi.org/10.5281/zenodo.5573294). While 3D-Slicer will be covered elsewhere, this hackathon explores neuroglancer as a possible extension to the current functionality accessible via OMERO.  

On the one hand, there is OMERO which is central to data management of different types of microscopic data as e.g. outlined above. On the other hand, **ARCs** (Annotated Research Contexts), offer - as indicated by its name - an annotated research context for multi-modal research projects conducted using methods across disciplines. However, imaging data and its metadata has not been covered well, so far.  
Here, we intend to bridge between OMERO and ARC and make use of the interoperability of both to enrich metadata and the research context on both sides.  

ARCs can open the door to the world of FAIR digital objects ([FDOs](https://zenodo.org/records/7782262)). Essentially, an ARC has according to its [specification](https://doi.org/10.5281/zenodo.10091038) a defined directory structure, adheres to several standards, is based on the [ISA model](https://doi.org/10.5281/zenodo.163640), can be versioned and enables workflows e.g. using Common Workflow Language ([CWL](https://doi.org/10.1145/3486897)) and [RO-Crate](https://doi.org/10.5281/zenodo.7867028) conversion. ARCs and respective supportive tools are developed by [DataPLANT](nfdi4plants.org).  

The Brain Imagin Data structure ([**BIDS**](https://doi.org/10.1038/sdata.2016.44)) provides some of the aspects mentioned above in order to handle complex and multi-modal neuroimaging and behavioural data. Key components are a formalized file and directory structure, use of controlled vocabulary, required metadata and BIDS Extension Proposals ([BEPs](https://bids-extensions.readthedocs.io/en/latest/guide/)).  

In order to properly manage and use imaging data, the availability of appropriate metadata is of utmost importance.  

While some metadata can be recorded by devices and automatically be extracted from the respective files or acquisition-specific file collections, other metadata need to be provided by the researcher to enable setting the imaging data in the appropriate research context. In particular, a well-defined set of metadata should be deposited when imaging data is submitted to a repository in order to preserve and to share it in a way following the principles of [FAIR](https://doi.org/10.1038/sdata.2016.18) (Findability, Accessibility, Interoperability, and Reusability). [**REMBI**](https://doi.org/10.1038/s41592-021-01166-8) (Recommended Metadata for Biological Images) is providing guidance on the content of such a well-defined set of metadata. Therefore, it is intended to explore REMBI with examples in the context of OMERO and ARC during this hackathon and to identify requirements obstacles for **mapping** metadata when transferring data between OMERO and ARC.  

The [NFDI4Bioimage Task Area 3](https://nfdi4bioimage.de/en/aims/task-areas/) (TA3) works on multimodal data linking and integration. It also prepares with this hackathon an upcoming [project on OMERO-ARC interoperability](https://www.denbi.de/de-nbi-events-archive/1614-towards-omero-and-arc-interoperability-for-rdm-compliant-bio-image-data) at the [2nd de.NBI BioHackathon](https://www.denbi.de/de-nbi-events-archive/1547-biohackathon-germany-2). (For more details on all contributors, please see the end of this file.)  


## Brief report about the event

In the following, a brief report about the event following the [schedule](./shared_pdfs/Cologne_Hackathon_Schedule.pdf) is provided.  

For in depth content, please see the individual talks, topics and follow-up work on OMERO-ARC interoperability (e.g. [here](https://github.com/NFDI4BIOIMAGE/BHG2023-OMERO-ARC)) and subsequent publications. In the end of this README, the contributors, respective links, organizers and funding statements can be founds. In between, you can find an overview of the repository content ([file tree](README.md#overview-of-the-content-in-this-repository)).  

Prior to the hackathon, some supportive installation informations including links targeted to the participants were shared for [OMERO](./Installation/OMERO/) (here only for Linux) and [ARC](./Installation/ARC/)-related installations.

### Setting the Stage

The first **NFDI4Bioimage - TA3-Hackathon** at CECAD at the University of Cologne was opened by Astrid Schauss, moderated by Andrea Schrader and the [TA3 opening presentation](./Introduction_Talks/opening-ta3-cologne-hackathon.pdf) was provided by Torsten Stöter.  

### Potential topics  

While preparing this Hackathon, we identified these potential topics for the Cologne Hackathon from a preparatory meeting with several participants:  

- [Interoperability OMERO-ARC (OMERO-BIDS, ARC-BIDS)](./Topics/Interoperability/)
- [REMBI / Mapping](./Topics/REMBI-Mapping/)
- [OMERO / zarr](./Topics/OMERO-zarr/)
- [3D Slicer, Neuroglancer](./Topics/3DSlicer_Neuroglancer/)

### Spot on the Topics

These and related topics were covered with introductory talks:  

- [OMERO and zarr (Joshua A. Moore)](./Introduction_Talks/intro-OMERO-zarr.pdf)
- [Annotated Research Context (ARC) (H. Lukas Weil)](./Introduction_Talks/BioimagingHackathon_2023_ARC.pdf)
- [Brain Imaging Data Structure (BIDS) (Julia Thönnißen)](./Introduction_Talks/BIDS.pdf)
- [3D Slicer, Neuroglancer (Torsten Stöter)](./Introduction_Talks/intro-3d-slicer-neuroglancer.pdf)
- [REMBI (Vanessa A. F. Fuchs, Tom Boissonnet)](./Introduction_Talks/2023-11-29_TA3-Hackathon_REMBI.pdf)

### Let the show(s) begin

#### Workflow and roadmap session(s)

In a workflow and roadmap session, graphical workflows were created, tasks were defined and the topics were selected.  

Beforehand, a [task list](./shared_pdfs/Cologne_Hackathon_Tasks.pdf) was created used as an inspiration and optionally to be adjusted for the different topics at the Hackathon (see [markdown version](./Topics/Cologne_Hackathon_Tasks.md) in the 'Topics' directory).  

#### Topic selection on-site

Following the initial intense discussions and task identification, some adjustments to the potential topics were made and the final topics on-site were selected:  

The interoperability topic focussed on **OMERO-ARC Interoperability**.  

3D Slicer and Neuroglancer are both covered in NFDI4Bioimage TA3 but only the **Neuroglancer** topic was eventually covered in this hackathon.  

The OMERO / zarr topic was represented as a topic in the Neuroglancer topic but not followed as an individual topic at this hackathon.  

The **REMBI** topic focusses on OMERO and ARC implementation concepts and on creating an example on-site.  

### Hacking - Documentation

Eventually, intensive work on the topics 'Interoperability', 'REMBI / Mapping', '3D Slicer / Neuroglancer (+OMEROzarr)' was conducted in groups.  

From the beginning, there was a focus on documentation and including use cases. The interoperability and REMBI topic served as preparatory work for a project at the 2nd de.NBI BioHackathon in Bielefeld: 'Towards OMERO and ARC interoperability for RDM-compliant bio-image data'.  

### Use Cases

A file for collecting [Use Cases](./Use_Cases.md) was created and filled.

### Shine!

The final reports summarized the outcome of the three groups.  
(Those presenting the work of the respective groups are provided in brackets.)  

- [Interoperability (H. Lukas Weil)](./Topics/Interoperability/Report/FinalReport_Interoperability.pdf)
- [REMBI / Mapping (Andrea Schrader, Tom Boissonnet)](./Topics/REMBI-Mapping/Report/FinalReport_REMBI_Mapping.pdf)
- [3D Slicer / Neuroglancer (+OMEROzarr) (Torsten Stöter)](./Topics/3DSlicer_Neuroglancer/Report/FinalReport_3DSlicer_Neuroglancer.pdf)

### 42?

We concluded with a discussion of all participants on where we found already answers and what needs to be solved in the future.  

### Closing the Hackathon

After closing the Hackathon from the organizational side (Andrea Schrader), Torsten Stöter summarized its content and Astrid Schauss, who hosted the hackathon at CECAD with the Cologne team, closed this hackathon that also bridged from NFDI4Bioimage to DataPLANT on the topic of OMERO-ARC interoperability.  

The interoperability and REMBI topic served as preparatory work for a project at the 2nd de.NBI BioHackathon Germany in Bielefeld: ['Towards OMERO and ARC interoperability for RDM-compliant bio-image data'](https://www.denbi.de/de-nbi-events-archive/1614-towards-omero-and-arc-interoperability-for-rdm-compliant-bio-image-data). The respective repository for this hackathon project is growing [here](https://github.com/NFDI4BIOIMAGE/BHG2023-OMERO-ARC).  

<br/>

---
---

## Overview of the content in this repository

```
.
├── CITATION.cff
├── CONTRIBUTING.md
├── Installation
│   ├── ARC
│   │   └── README.md
│   └── OMERO
│       └── README.md
├── Introduction_Talks
│   ├── 2023-11-29_TA3-Hackathon_REMBI.pdf
│   ├── BIDS.pdf
│   ├── BioimagingHackathon_2023_ARC.pdf
│   ├── BioimagingHackathon_2023_ARC.pptx
│   ├── README.md
│   ├── intro-3d-slicer-neuroglancer.pdf
│   ├── intro-OMERO-zarr.pdf
│   ├── intro-OMERO-zarr.pptx
│   └── opening-ta3-cologne-hackathon.pdf
├── LICENSE
├── README.md
├── Topics
│   ├── 3DSlicer_Neuroglancer
│   │   ├── README.md
│   │   ├── Report
│   │   │   └── FinalReport_3DSlicer_Neuroglancer.pdf
│   │   └── images
│   │       ├── 3Dslicer_Neuroglancer.jpeg
│   │       ├── Screenshot 2023-12-01 115118.png
│   │       ├── Screenshot at 2023-11-30 17-24-16.png
│   │       └── Screenshot_2023-11-30_17-15-43.png
│   ├── Cologne_Hackathon_Tasks.md
│   ├── Interoperability
│   │   ├── OMERO-ARC-Exporter-WorkFlow-Introduction.pdf
│   │   ├── Omero-ARC-topic-'use-cases'.pdf
│   │   ├── README.md
│   │   ├── Report
│   │   │   └── FinalReport_Interoperability.pdf
│   │   ├── images
│   │   │   ├── Interoperability.jpeg
│   │   │   └── Interoperability_progress.jpg
│   │   ├── omero_arc_connection.md
│   │   ├── omero_arc_exporter.md
│   │   └── omero_arc_mapping.md
│   ├── OMERO-zarr
│   │   ├── README.md
│   │   └── images
│   │       └── OMERO_zarr.jpeg
│   └── REMBI-Mapping
│       ├── README.md
│       ├── REMBI-template_CAi_VF.xlsx
│       ├── REMBI-template_CAi_VF_AS.xlsx
│       ├── Report
│       │   └── FinalReport_REMBI_Mapping.pdf
│       └── images
│           └── REMBI_Mapping.jpeg
├── Use_Cases.md
└── shared_pdfs
    ├── Cologne_Hackathon_Schedule.pdf
    └── Cologne_Hackathon_Tasks.pdf
```
16-01-2024 (created using [tree](https://oldmanprogrammer.net/source.php?dir=projects/tree) v2.1.1 © 1996 - 2023 by Steve Baker, Thomas Moore, Francesc Rocher, Florian Sesser, Kyosuke Tokoro)

<br/>

---
---

## Contributions

**Optimal contribution during the Hackathon was suggested [here](CONTRIBUTING.md).**

 <br />

🙌 Thank you for any contribution to the **NFDI4Bioimage - TA3-Hackathon - UoC-2023** repository!!!  

When contributing, participants were asked to consider that (parts of) this repository might be used by people with various background and intentions including teaching in the future. Therefore, it is appreciated if  ***a brief non-specialist targeted introduction / summary*** was provided preceding the respective content or is added after the hackathon to complete these sections.  


### Contributors in alphabetical order

🤝 Participants contributing to the **NFDI4Bioimage - TA3-Hackathon - UoC-2023** could provide their name, GitHub handle, ORCID iD and ROR right here in the README - if they liked.  

|name|GitHub|ORCID|ROR|  
|---|---|---|---|  
|Niraj Kandpal|[@Nirkan](https://github.com/Nirkan)|https://orcid.org/0009-0007-5101-4786|[https://ror.org/00rcxh774](https://ror.org/00rcxh774) <br>[https://ror.org/04c4bwh63](https://ror.org/04c4bwh63)|
|Christoph Möhl|[@cmohl2013](https://github.com/cmohl2013)|https://orcid.org/0000-0002-0829-5101||
|Josh Moore|[@joshmoore](https://github.com/joshmoore)|https://orcid.org/0000-0003-4028-811X|[https://ror.org/05tpnw772](https://ror.org/05tpnw772)|
|Astrid Schauss|[@AstridSchauss](https://github.com/AstridSchauss)|[https://orcid.org/0000-0002-6658-2192](https://orcid.org/0000-0002-6658-2192)|[https://ror.org/00rcxh774](https://ror.org/00rcxh774) <br>[https://ror.org/04c4bwh63](https://ror.org/04c4bwh63) |
|Andrea Schrader|[@andreaschrader](https://github.com/andreaschrader)|https://orcid.org/0000-0002-3879-7057|https://ror.org/034waa237<br><br>https://ror.org/00rcxh774| 
|Torsten Stöter|[@tstoeter](https://github.com/tstoeter)||[https://ror.org/01zwmgk08](https://ror.org/01zwmgk08)| 
|Julia Thönnißen|[@JThoennissen](https://github.com/JThoennissen)|[https://orcid.org/0000-0002-5467-871X](https://orcid.org/0000-0002-5467-871X)|| 
|Monica Valencia-Schneider|[@mvals](https://github.com/mvals)|[https://orcid.org/0000-0003-3430-2683](https://orcid.org/0000-0003-3430-2683)|[https://ror.org/00rcxh774](https://ror.org/00rcxh774)|
|Heinrich Lukas Weil|[@HLWeil](https://github.com/HLWeil)|[https://orcid.org/0000-0003-1945-6342](https://orcid.org/0000-0003-1945-6342)|[https://ror.org/01qrts582](https://ror.org/01qrts582)|
|Peter Zentis|[@pzentis](https://github.com/pzentis)|[https://orcid.org/0000-0002-6999-132X](https://orcid.org/0000-0002-6999-132X)|[https://ror.org/00rcxh774](https://ror.org/00rcxh774) <br>[https://ror.org/04c4bwh63](https://ror.org/04c4bwh63) |

## Zenodo submission

The full list of participants - some only contributing to conceptual work on site and not directly to this repo - is provided in the [CITATION.cff](./CITATION.cff) and [.zenodo.json](./\.zenodo.json) files.  

CITATION.cff and .zenodo.json:
- CITATION.cff is used as a citation being directly in the repository and being accessible via the GitHub sidebar. 
- Citation.cff was tested with [cffconvert](https://github.com/citation-file-format/cffconvert) prior to adding the references to be valid.  
- The repo is prepared to be submitted as described [here](https://github.com/andreaschrader/doi-exercise) or [here](https://coderefinery.github.io/github-without-command-line/doi/). .zenodo.json is used for transferring the contained metadata to Zenodo.  

## Organizers

Eik Dahms, Niraj Kandpal, Astrid Schauss, Andrea Schrader, Torsten Stöter, Monica Valencia-Schneider, Peter Zentis (alphabetical order)

## Acknowledgement

We would like to acknowledge the support from the NFDI4Bioimage, in particular TA3, TA1 and TA5 and in particular all participants to make this hackathon happen.  

For the OMERO-ARC topic, we are thankful for the collaboration with DataPLANT. We acknowledge Timo Mühlhaus in discussions during planning for the OMERO-ARC project and Kevin Schneider in preparatory meetings on the OMERO-ARC project (both: DataPLANT).

We thank Heinrich Lukas Weil (DataPLANT) for participating and contributing as a guest, also providing the introductory talk on ARC.

Moreover, we thank the RRZK (Daniel Wickeroth) for presenting and explaining the [CAVE](https://rrzk.uni-koeln.de/en/hpc-projects/visualization/cave) to the hackathon participants!

## Funding - for this hackathon
(funding for the event and enabling for organization and participation)

### NFDI4Bioimage
Funded by the German Research Foundation (DFG) within the framework of the NFDI – project numbers: 501864659.

### Other Organisations
#### CEPLAS
Funded by the Deutsche Forschungsgemeinschaft (DFG, German Research Foundation) within Germany’s Excellence Strategy – EXC-2048/1 – project number 390686111.

#### CECAD
Funded by the Deutsche Forschungsgemeinschaft (DFG, German Research Foundation) under Germany's Excellence Strategy - EXC 2030 - 390661388.

#### CRC TRR341
Funded by the Deutsche Forschungsgemeinschaft (DFG, German Research Foundation) – Project-ID 456082119.