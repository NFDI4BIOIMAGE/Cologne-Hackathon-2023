<h1 style="text-align: center;">NFDI4Bioimage - TA3-Hackathon - UzK-2023</h1>

***<p style="text-align: center;">29.11.- 01.12.2023</p>*** 

**<p style="text-align: center;">Location: CECAD, Joseph-Stelzmann-Str.26, 50931 Cologne</p>**  

## <center>- T A S K    L I S T S -</center>

### <center>List of tasks for hacking for the 4 topics:</center>
#### <center><p style="color:blue">1. Interoperability OMERO-ARC (OMERO-BIDS, ARC-BIDS)</p></center>
#### **<center><p style="color:green"><ins>2.	REMBI / Mapping</ins></p></center>** 
#### ***<center><p style="color:red"><ins>3.	OMERO / zarr</ins></p></center>***
#### ***<center>4.	3D Slicer, Neuroglancer</center>***


<h4 style="color:blue;">
    ARC / OME<!-- 
--><span style="color:red;"><b><ins><i>RO</i></b></span><!-- 
--><span style="color:black;"> + </span><!-- 
--><span style="color:green;"><b><ins>REMBI/Mapping</ins></b></span>
</h4>

**WIP**

##### Outline of the project

![REMBI_image](./images/REMBI_Mapping.jpeg)

##### **Questions**  
  
- Should REMBI go into an ARC?
- Can we map ARC metadata to a REMBI template?
- Can we cherrypick the metadata of the ARC to extract the REMBI aligned metadata?
- Try to find out which metadata is required when submitting to an imaging repository that expect users to use REMBI?

##### Outcome

- Everyone got much more acquainted with the concepts and tools
  - guidance for OMERO, learned about REMBI template used @CAi, navigated in an ARC, Explored possibilities in Swate and discussed about the use of templates and appropriate ontology.  
  - Still some installations are required.

- Started documentation of the current state of the art and the steps done for this topic at the Cologne Hackathon.
- Collected possible issues for OMERO-ARC users:
  - How to import images/stacks in OMERO
  - Organization of data in OMERO (project/dataset compared to tags vs. key-value-pairs) for easier mapping to and from ARC.
- "for Christoph": How to handle "tags" in OMERO -> selection of metadata (subsets) for an ARC
- Possible combination of workflows and runs triggered from an ARC with OMERO and tools consuming input data from OMERO, retrieving output data and exporting this again into an ARC. Does this make sense?

Started bringing a dataset from the [example ARC](https://git.nfdi4plants.org/natural-variation-and-evolution/microscopy_collection/map-by-seq_clsm-stacks) into OMERO.  

##### Outlook
- Using Peter's current "Import KV from csv" (https://github.com/cecad-imaging/omero-arc-testdata/tree/main) in OMERO to import the key-value pairs from an ARC-style isa.investigation.xlsx
- Maybe easier or already done above: Go the reverse way, i.e. do all above steps for export out of OMERO into structure
  - Use the [OMERO-ARC exporter](https://github.com/cmohl2013/omero-cli-transfer/tree/arc)


tbc


##### **Tasks**  

- Get OMERO running on the institutional instance.

- Which part of the dataset can we directly see inside OMERO, which not? Any ideas for support? 
  - No directory structure
  - xml files need to be added as attachment
    - This is because any non-bioformats compatible file needs to be added as an attachment.

- Try adhering to REMBI for the metadata.
  - Filling a REMBI template based on CAi experience for the [imaging ARC](https://git.nfdi4plants.org/natural-variation-and-evolution/microscopy_collection/map-by-seq_clsm-stacks).

- Which steps are necessary to achieve automatic import?
    - Outlines strategies for mapping of microscopy related metadata (including REMBI alined metadata) between ARC and OMERO.