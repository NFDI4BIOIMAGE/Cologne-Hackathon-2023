## 3 approaches with increasing complexity

30.11.23_Morning discussion

### Reference model

OMERO and/or ARC store reference IDs (URLs) of the data objects in the other Database.

This would technically be the easiest solution, but specifications need to be updated. More hard constrain: Do we want, to have data and metadata split, with the possibility of links pointing to nothing in the future?

### Snapshot model

On demand snapshotting of information of one model and putting it into the other. The user decides when and what information to merge into what.

The is great control wise and might be very flexible in general. Snapshots could of course be exported from and imported into other tools as well.

The downside is, that desynchronization might occur.

### Synchronization model

Full information is stored in OMERO and DataHub, and being directly synchronized with each other.

This would be the holy grail solution, where users select their tool based on the current goal they have, and changes also appear on the other one.

Technically, this is very difficult to implement. Merge-conflicts might be showstopper.

## General thoughts

- Transfer of objects between DataHub and OMERO should be possible without having the data objects on the users computer by making use of git-lfs hashes.

- An image file does not know itself, how many images it contains. Therefore, changing content of image files after they are created will in many cases cause big problems in OMERO.
  
  - Read-only files or folders specified in some config?
  - Create new identities in OMERO?
  - `Raw data file` headers specify files which may not be modified?
  


