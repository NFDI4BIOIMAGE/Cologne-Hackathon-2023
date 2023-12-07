# Omero ARC Exporter

A CLI tool to export Omero projects to arc is currently developed as a plugin of
[omero-cli-transfer](https://github.com/ome/omero-cli-transfer):

[omero-cli-transfer with arc export option](https://github.com/cmohl2013/omero-arc)


## Workflow

Two options:
* Create a new ARC from an Omero project
* Add an Omero project as new study and associated Assays (Omero datasets) to an existing ARC.

```
omero transfer pack --plugin arc Project:1343 path/to/my/new_arc
omero transfer pack --plugin arc Project:1343 path/to/my/existing_arc
```

## Omero-ARC-Mapping in the current version

There are countless possibilities how Omero data could mapped to an ARC, and there are countless good reasons for each possibility. This may lead to the idea, that the decision should be left to the user how he/she wants to route their data from Omero to ARC. I do not think, that this is a good idea:

* A software that leaves many decisions to the user is hard to use.
* A software that has many configuration options is hard to test and therefore likely to be buggy.

As software developers, we want our software to be used by many people. Hard to use and buggy software is not likely to be used.

Therefore, we took decisions how to map Omero data to ARC repositories. These decisions are preliminary. In fact, we expect that the routing in the current version is very likely to be changed. However, you have to start at some point. The software is designed in a way, that data mapping can be easily changed.

### Routing configuration
The routing of all key-value pairs is currently defined in the mapper classes:

* `IsaInvestigationMapper`
* `IsaStudyMapper`
* `IsaAssayMapper`
* `IsaAssaySheetMapper`

https://github.com/cmohl2013/omero-cli-transfer/blob/arc/src/arc_mapping.py

The data is stored in the Omero project and associated datasets in mapped annotations matching a specific namespace. If mapped annotations are not present, default values are set that are taken from the omero model. E.g. if the study title is not defined in a mapped annotation, the Omero project title is used instead.

* Omero Project -> ISA Study
* Omero Dataset -> ISA Assay
* Omero Image -> ISA Dataset

The metadata from ISA Investigation is currently stored in mapped annotations on the Omero project level (e.g. investigation identifier)
