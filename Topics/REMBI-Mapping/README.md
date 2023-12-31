# REMBI - Mapping

## Introduction / Summary

**REMBI** is the abbreviation for **RE**commended **M**etadata for **B**iological **I**mages

The REMBI publication can be read here: https://rdcu.be/dsDc6.  
At this Hackathon, we used a REMBI template which is used at CAi at HHU Duesseldorf.  
The CAi REMBI template is adapted from the REMBI table in the supplementary information of the REMBI publication: https://doi.org/10.1038/s41592-021-01166-8.


## Workflow session
First connections of REMBI with ARC and OMERO.

<!---The workflow session could be explained here and how the drawings at the boards evolved.\--->

<!---could be converted to a digital version, use ARC/ISA-specific terms (study, assay, source first, sample last)\--->

![REMBI_image](./images/REMBI_Mapping.jpeg)

## Results

### Following the suggested [**Tasks**](../Cologne_Hackathon_Tasks.md)  

- Get OMERO running on the institutional instance.

- Which part of the dataset can we directly see inside OMERO, which not? Any ideas for support? 
  - No directory structure
  - xml files need to be added as attachment
    - This is because any non-bioformats compatible file needs to be added as an attachment.

- Try adhering to REMBI for the metadata.
  - Filling a REMBI template based on CAi experience for the [imaging ARC](https://git.nfdi4plants.org/natural-variation-and-evolution/microscopy_collection/map-by-seq_clsm-stacks).

- Which steps are necessary to achieve automatic import?
    - Outline strategies for mapping of microscopy related metadata (including REMBI aligned metadata) between ARC and OMERO.

### **Questions**  
  
- Should REMBI go into an ARC?
- Can we map ARC metadata to a REMBI template?
- Can we cherrypick the metadata of the ARC to extract the REMBI aligned metadata?
- Try to find out which metadata is required when submitting to an imaging repository that expect users to use REMBI?

### Progress

- Everyone got much more acquainted with the concepts and tools
  - guidance for OMERO, learned about REMBI template used @CAi, navigated in an ARC, explored possibilities in Swate and discussed about the use of templates and appropriate ontology.  
  - Still some installations are required.

- Started documentation of the current state of the art and the steps done for this topic at the Cologne Hackathon.
- Collected possible issues for OMERO-ARC users:
  - How to import images/stacks in OMERO
  - Organization of data in OMERO (project/dataset compared to tags vs. key-value-pairs) for easier mapping to and from ARC.
- related to the omero-arc-exporter: How to handle "tags" in OMERO -> selection of metadata (subsets) for an ARC
- Possible combination of workflows and runs triggered from an ARC with OMERO and tools consuming input data from OMERO, retrieving output data and exporting this again into an ARC. Does this make sense?

Started bringing a dataset from the [example ARC](https://git.nfdi4plants.org/natural-variation-and-evolution/microscopy_collection/map-by-seq_clsm-stacks) into OMERO. 

## [Report](./Report/)

The final report at the last day of the hackathon for the Interoperability topic can be found [here](./Report/FinalReport_REMBI_Mapping.pdf).

## Outlook
- Using Tom's ["Import KV from csv" ](https://github.com/German-BioImaging/omero-scripts/blob/xtnd_support_kvpairs/omero/annotation_scripts/) in OMERO to import the key-value pairs from csv files extracted from an ARC-style isa.investigation.xlsx with Peter's [script](https://github.com/cecad-imaging/omero-arc-testdata/blob/main/scripts/isaToKVP.py)
- Maybe easier or already done above: Go the reverse way, i.e. do all above steps for export out of OMERO into structure
  - Use the [OMERO-ARC exporter](https://github.com/cmohl2013/omero-cli-transfer/tree/arc)
