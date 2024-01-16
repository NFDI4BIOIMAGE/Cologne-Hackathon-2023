# 👋 Cologne-Hackathon-2023

[![License: CC BY 4.0](https://img.shields.io/badge/License-CC_BY_4.0-lightgrey.svg)](https://creativecommons.org/licenses/by/4.0/)  

This is the repository for documentation during the first **NFDI4Bioimage - TA3-Hackathon - UoC-2023** (in short: **Cologne Hackathon**).  

Prior to the hackathon, some supportive installation informations including links targeted to the participants were shared for [OMERO](./Installation/OMERO/) (here only for Linux) and [ARC](./Installation/ARC/)-related installations.

In the following, a brief report about the event following the [schedule](./shared_pdfs/Cologne_Hackathon_Schedule.pdf) is provided.  

For in depth content, please see the individual talks, topics and follow-up work on OMERO-ARC interoperability (e.g. [here](https://github.com/NFDI4BIOIMAGE/BHG2023-OMERO-ARC)) and subsequent publications. In the end of this README, the contributors, respective links, organizers and funding statements can be founds. In between, you can find an overview of the repository content ([file tree](README.md#overview-of-the-content-in-this-repository)).  

## Setting the Stage

The first **NFDI4Bioimage - TA3-Hackathon** at CECAD at the University of Cologne was opened by Astrid Schauss, moderated by Andrea Schrader and the [TA3 opening presentation](./Introduction_Talks/opening-ta3-cologne-hackathon.pdf) was provided by Torsten Stöter.  

## Potential topics  

While preparing this Hackathon, we identified these potential topics for the Cologne Hackathon from a preparatory meeting with several participants:  

- [Interoperability OMERO-ARC (OMERO-BIDS, ARC-BIDS)](./Topics/Interoperability/)
- [REMBI / Mapping](./Topics/REMBI-Mapping/)
- [OMERO / zarr](./Topics/OMERO-zarr/)
- [3D Slicer, Neuroglancer](./Topics/3DSlicer_Neuroglancer/)

## Spot on the Topics

These and related topics were covered with introductory talks:  

- [OMERO and zarr (Joshua A. Moore)](./Introduction_Talks/intro-OMERO-zarr.pdf)
- [Annotated Research Context (ARC) (H. Lukas Weil)](./Introduction_Talks/BioimagingHackathon_2023_ARC.pdf)
- [Brain Imaging Data Structure (BIDS) (Julia Thönnißen)](./Introduction_Talks/BIDS.pdf)
- [3D Slicer, Neuroglancer (Torsten Stöter)](./Introduction_Talks/intro-3d-slicer-neuroglancer.pdf)
- [REMBI (Vanessa A. F. Fuchs, Tom Boissonnet)](./Introduction_Talks/2023-11-29_TA3-Hackathon_REMBI.pdf)

## Let the show(s) begin

### Workflow and roadmap session(s)

In a workflow and roadmap session, graphical workflows were created, tasks were defined and the topics were selected.  

Beforehand, a [task list](./shared_pdfs/Cologne_Hackathon_Tasks.pdf) was created used as an inspiration and optionally to be adjusted for the different topics at the Hackathon (see [markdown version](./Topics/Cologne_Hackathon_Tasks.md) in the 'Topics' directory).  

### Topic selection on-site

Following the initial intense discussions and task identification, some adjustments to the potential topics were made and the final topics on-site were selected:  

The interoperability topic focussed on **OMERO-ARC Interoperability**.  

3D Slicer and Neuroglancer are both covered in NFDI4Bioimage TA3 but only the **Neuroglancer** topic was eventually covered in this hackathon.  

The OMERO / zarr topic was represented as a topic in the Neuroglancer topic but not followed as an individual topic at this hackathon.  

The **REMBI** topic focusses on OMERO and ARC implementation concepts and on creating an example on-site.  

## Hacking - Documentation

Eventually, intensive work on the topics 'Interoperability', 'REMBI / Mapping', '3D Slicer / Neuroglancer (+OMEROzarr)' was conducted in groups.  

From the beginning, there was a focus on documentation and including use cases. The interoperability and REMBI topic served as preparatory work for a project at the 2nd de.NBI BioHackathon in Bielefeld: 'Towards OMERO and ARC interoperability for RDM-compliant bio-image data'.  

## Use Cases

A file for collecting [Use Cases](./Use_Cases.md) was created and filled.

## Shine!

The final reports summarized the outcome of the three groups.  
(Those presenting the work of the respective groups are provided in brackets.)  

- [Interoperability (H. Lukas Weil)](./Topics/Interoperability/Report/FinalReport_Interoperability.pdf)
- [REMBI / Mapping (Andrea Schrader, Tom Boissonnet)](./Topics/REMBI-Mapping/Report/FinalReport_REMBI_Mapping.pdf)
- [3D Slicer / Neuroglancer (+OMEROzarr) (Torsten Stöter)](./Topics/3DSlicer_Neuroglancer/Report/FinalReport_3DSlicer_Neuroglancer.pdf)

## 42?

We concluded with a discussion of all participants on where we found already answers and what needs to be solved in the future.  

## Closing the Hackathon

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
16-01-2024

## Contributions

**Optimal contribution during the Hackathon was suggested [here](CONTRIBUTING.md).**

 <br />

🙌 Thank you for any contribution to the **NFDI4Bioimage - TA3-Hackathon - UoC-2023** repository!!!  

When contributing, participants were asked to consider that (parts of) this repository might be used by people with various background and intentions including teaching in the future. Therefore, it is appreciated if  ***a brief non-specialist targeted introduction / summary*** was provided preceding the respective content or is added after the hackathon to complete these sections.  


## Contributors in alphabetical order

🤝 Participants contributing to the **NFDI4Bioimage - TA3-Hackathon - UoC-2023** could provide their name, GitHub handle, ORCID iD and ROR right here in the README - if they liked. The full list of participants - some only contributing to conceptual work on site and not directly to this repo - is provided in the [CITATION.cff](./CITATION.cff) and [.zenodo.json](./\.zenodo.json) files.  

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

## Organizers

Eik Dahms, Niraj Kandpal, Astrid Schauss, Andrea Schrader, Torsten Stöter, Monica Valencia-Schneider, Peter Zentis (alphabetical order)

## Acknowledgement

We would like to acknowledge the support from the NFDI4Bioimage, in particular TA3, TA1 and TA5 and in particular all participants to make this hackathon happen.  

For the OMERO-ARC topic, we are thankful for the collaboration with DataPLANT. We acknowledge Timo Mühlhaus in discussions during planning for the OMERO-ARC project and Kevin Schneider in preparatory meetings on the OMERO-ARC project (both: DataPLANT).

We thank Heinrich Lukas Weil (DataPLANT) for participating and contributing as a guest, also providing the introductory talk on ARC.

Moreover, we thank the RRZK (Daniel Wickeroth) for presenting and explaining the [CAVE](https://rrzk.uni-koeln.de/en/hpc-projects/visualization/cave) to the hackathon participants!

## Funding - for this Hackathon
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