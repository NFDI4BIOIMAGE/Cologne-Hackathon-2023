## OMERO <-> ARC mapping

30.11.23_Afternoon discussion


## General thoughts

- Files and images are a N to M mapping.

  In order to represent the measurement of a sample resulting in the creation of a specific image, pointing to the file is not enough. 
  
  Maybe this could be solved by data fragment selectors (see [PR on ISA](https://github.com/ISA-tools/isa-specs/pull/15)). Probably there would be a selector syntax needed for each file format.

  Also in some cases it would be more practical to have the `Image File` column point to a directory instead. Does this break ISA/ARC?

- Image file metadata extraction

  Each imaging device produces a file format with a lot information (can easily be 1000 properties). BIO-FORMATS is a tool which extracts image information from different file formats. Additionally to this, it preselects properties that fit into the OME model ([check here](https://bio-formats.readthedocs.io/en/stable/supported-formats.html)). 

  These could be used as a basis of metadata mapped into an ARC. The full metadata might be too big and specific for the general registry.

  Some properties that are not part of OME xml might still be of interest and their mapping to ISA could be hard coded.


