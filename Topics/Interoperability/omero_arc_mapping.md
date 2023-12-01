# OMERO <-> ARC mapping

## General thoughts

- Files and images are a N to M mapping.

  In order to represent the measurement of a sample resulting in the creation of a specific image, pointing to the file is not enough. 
  
  Maybe this could be solved by data fragment selectors (see [PR on ISA](https://github.com/ISA-tools/isa-specs/pull/15)). Probably there would be a selector syntax needed for each file format.

  Also in some cases it would be more practical to have the `Image File` column point to a directory instead. Does this break ISA/ARC?

- Natively mappable properties should be only natively mapped
  
  As a native property in a schema we define a property that has a fixed key. Natively mappable then means that the same piece of information has a specific place and key in both schemas. 

## Images

- Image file metadata extraction

  Each imaging device produces a file format with a lot information (can easily be 1000 properties). BIO-FORMATS is a tool which extracts image information from different file formats. Additionally to this, it preselects properties that fit into the OME model ([check here](https://bio-formats.readthedocs.io/en/stable/supported-formats.html)). 

  These could be used as a basis of metadata mapped into an ARC. The full metadata might be too big and specific for the general registry. We call the fields we use the "reasonable subset":
    
  - Acquisition/Microscope
  - Acquisition/Image

  Some properties that are not part of OME xml might still be of interest and their mapping to ISA could be hard coded.

- OMERO native image metadata can be mapped to parameter columns in annotation tables in ISA:

  Where the ontology terms for the annotation tables come from needs to be decided. Maybe they exist in OME.owl or are general enough to exist in an external ontology. 

- OMERO image metadata as annotation table columns in ISA:

  - Description
  - Acquisition/Microscope
  - Acquisition/Image
  - Tags (Header key "Tag")
  - Key-Value Pairs
  - Attachments/Tables are files, this is pretty tricky
  - Comments could be a bit tricky in ARC

- OMERO Channels and Regions of interest are more difficult to map
 
  - For every image there might be multiple channels (e.g. RGB). Maybe data fragment selector in ISA could point to channel instead of file?

  - Regions of Interest are marked areas on a file or channel. They are stored as a list of coordinates. This might be the line we draw for storing the metadata.

## Container mapping

In general, we can't know specific separation rules for when to further split up OMERO containers into ARC objects beyond the general rules described below. But maybe this could be enhanced with some additional annotation (optional) on OMERO.

### Project-Dataset

  - This is probably the more easier of the two

  - `Project` maps to `Study` (1to1)

  - `Datasets` maps to `Assays` (NtoN)

  - `Images` are `Rows` (NtoN) (According to the rules defined [above](#images))

### Screen-Plate-Well

  - `Screen` maps to `Study` (1to1)

  - `Plates` map to an `Assay` (Nto1)

  - `Wells` map to `Materials` in the process Graph (NtoN) (Exact location in ARC tbd)

  - `Well location` is mapped to a `Parameter` of the process ()

  - `Images` are `Rows` (NtoN), being measurement outputs of the `Well`



