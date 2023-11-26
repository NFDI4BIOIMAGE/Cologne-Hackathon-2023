<h1 style="text-align: center;">NFDI4Bioimage - TA3-Hackathon - UzK-2023</h1>

***<p style="text-align: center;">29.11.- 01.12.2023</p>*** 

**<p style="text-align: center;">Location: CECAD, Joseph-Stelzmann-Str.26, 50931 Cologne</p>**  

## <center>- T A S K    L I S T S -</center>

**<center>List of tasks for hacking for each of the 4 topics:</center>**  
#### <center><p style="color:blue">1. Interoperability OMERO-ARC (OMERO-BIDS, ARC-BIDS)</p></center>
#### **<center><p style="color:green"><ins>2.	REMBI / Mapping</ins></p></center>** 
#### **<center><p style="color:red">3.	OMERO / zarr</p></center>**
#### ***<center>4.	3D Slicer, Neuroglancer</center>***

For each of the topics, please use and adapt as much as possible from the tasks in this document and extend these where required. Please adapt this document accordingly in the respective part of the GitHub directory to create your tasks for the Hackathon and an optional outlook.  

Different team members can work on different tasks from your list.  

Please make sure that everybody in your team has a tasks to contribute to and document progress.  

One task for all: Decide until the end of the Hackathon which parts of your work can be set public and which, if any, have to stay private and let us know.  

**Mandatory: Documentation**  

🙌 Thank you!

<br>
<br>
<br>

Task usually build on top of another, but some can be worked on independently

<h4 style="color:blue;">
    BIDS/ARC<!-- 
--><span style="color:black;">/</span><!-- 
--><span style="color:red;"><strong>zarr</strong></span><!-- 
--><span style="color:black;"> + </span><!-- 
--><span style="color:green;"><strong><ins>REMBI/Mapping</ins></strong></span>
</h4>

Bring/take your own data set and put it into ARC / BIDS / zarr manually or using existing tools  

##### **Tasks**  

- Read docs and specs, get tools running and installed  
- Document the steps from status quo of dataset to structured final result  
- Where were problems, uncertainties, questions? Could these be resolved? How?  
- Try implementing REMBI during this procedure  


##### **Goals**  

- Everyone gets much more acquainted with the concepts and tools.  
- This can serve as hands-on examples for teaching later:  
  - Provide documentation of the current state of the art and the steps done in the selected tasks.
- We get more sample data for development and testing:  
  - Create/add public use cases / examples.

<h4 style="color:blue;">
    OME<!-- 
--><span style="color:red;"><strong>RO</strong></span><!-- 
--><span style="color:black;"> + </span><!-- 
--><span style="color:green;"><strong><ins>REMBI/Mapping</ins></strong></span>
</h4>

The next level is to bring your newly structured dataset into OMERO.  

##### **Tasks**  

- Get OMERO running on your own system (Docker) or your institutional instance.
- Which OMERO setup is necessary, i.e. which plugins and additional tools are required?
- Which part of the dataset can we directly see inside OMERO, which not? Any ideas for support?
- Again all steps should be documented
- Try adhering to REMBI for the metadata.
- Which steps are necessary to achieve automatic import?
- Identify missing UI features in OMERO for (meta)data presentation or import step. How can the UI support more?
- Maybe easier or already done above: Go the reverse way, i.e. do all above steps for export out of OMERO into structure
- Even further level: Start writing a script for automatic import/export maybe more or less tailored to your specific example, later generalize from there – align this with Christoph’s work who is working on OMERO-ARC export: https://github.com/cmohl2013/omero-cli-transfer/tree/arc.  

##### **Goals**  

- Provide documentation of the current state of the art and the steps done in the selected tasks.
- Create/add public use cases / examples.
- Get development going for ARC/OMERO interoperability for the de.NBI BioHackathon topic (https://www.denbi.de/de-nbi-events/1614-towards-omero-and-arc-interoperability-for-rdm-compliant-bio-image-data)

<h4 style="color:red;">
    <strong>OMERO/zarr</strong><!-- 
--><span style="color:black;"> + <i><strong>Neuroglancer</strong></i> (+ </span><!-- 
--><span style="color:green;"><strong><ins>REMBI/Mapping</ins></strong></span><!-- 
--><span style="color:black;">)</span>
</h4>

Integrate Neuroglancer with OMERO (Slicer mostly covered by external partner)  

##### **Tasks**  

- Get Neuroglancer running on its own and do some 3D visualization of your or example dataset
- What are the requirements for it to work? Server/client setup, file format, browser, …
- Get OMERO running on your own system (Docker) or your institutional instance
- Use omero-web-zarr to export zarr from OMERO, get it working. OMERO will provide a zarr-URL.
- Can we load this zarr-URL directly in Neuroglancer? If not how can we bridge (or transfer) from OMERO to Neuroglancer?
- Add a button or context menu to OMERO for loading in Neuroglancer. See examples and build on omereo-web-zarr plugin.
- If things go very well compile an OMERO plugin for this or commit changes to omero-web-zarr
- Do we want to store results from visualization back into OMERO? If so where and how?
- Which metadata (according to REMBI) needs to be added (OMERO key-value pairs/to ARCs) when using Neuroglancer (zarr).
- Again document everything necessary for reproducing our results to make it usable for teaching

##### **Goals**  

- Getting better 3D visualization in OMERO.
- Provide documentation of the steps needed for this.
- Create a public use case / example.