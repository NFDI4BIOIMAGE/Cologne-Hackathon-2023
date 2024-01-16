# Installation and instructions

## DataPLANT HUB (GitLab)

Please [**sign up**](https://auth.nfdi4plants.org/realms/dataplant/login-actions/registration?client_id=gitlab-fr&tab_id=4ePYMBSqVBU) for access to the DataPLANT HUB! As this link might change over time, follow the link to the DataHUB from the [DataPLANT website](https://nfdi4plants.org/) in case the **sign up** link provided above it is not active anymore  

- For installation instructions, please see below.

Here you can start to dive into the ARCiverse:  

> In case these links change in the future, please search yourself through the [DataPLANT Knowledge Base](https://nfdi4plants.org/nfdi4plants.knowledgebase/index.html) for the respective information.  


- create an ARC (either in the HUB with a template or locally e.g. using the [ARC commander](https://nfdi4plants.org/nfdi4plants.knowledgebase/docs/ArcCommanderManual/arc_initialization.html) (`arc init`)
- sync once an ARC with the HUB - do not worry about failing pipelines - arc validation is under constructions
- add at least one building block using [Swate](https://nfdi4plants.org/nfdi4plants.knowledgebase/docs/SwateManual/index.html) (here is the link to the [Swate repo](https://github.com/nfdi4plants/Swate)) or [Swate alpha](https://swate-alpha.nfdi4plants.org/).
- [Grow-an-ARC](https://git.nfdi4plants.org/andreaschrader/Grow-an-ARC_Example) - example for filling the isa.investigation file using ARCcommander v0.5.0 - WIP
- A [simple microscopy ARC](https://git.nfdi4plants.org/natural-variation-and-evolution/microscopy_collection/map-by-seq_clsm-stacks) in the making and used as a template for Grow-an-ARC - WIP
- A nice example: [Michele's ARC](https://git.nfdi4plants.org/michele.bortolomeazzi/mben_resolve)

## ARCcommander

Respository: https://github.com/nfdi4plants/ARCCommander   
Knowledge Base: https://nfdi4plants.org/nfdi4plants.knowledgebase/docs/ArcCommanderManual/index.html   

## Installing the suggested **(preview) version of the ARCcommander**

### Requirements (ARC Commander)
**git**  
**git-lfs**  

Please note, the installation as described below was tested before the hackathon end of November 2023. There might be changes thereafter.

Installing the preview2 for v1.0.0 of the ARCcommander for experienced users (just execute the code block in 3. And check the name of the version you want to install) and with more detailed comments for beginners:

Please select and download here: https://github.com/nfdi4plants/ARCCommander/releases the version you want to install.

Remove the old ARC commander version if not in `/usr/local/bin/` but anywhere else on the system.

### Tested for macOS:

1.	Download the x64 version from [here](https://github.com/nfdi4plants/ARCCommander/releases) into the Download directory: arc_osx-x64 
You have to adjust accordingly the second line in point 3 below in case the name name of the downloaded file (here `arc_osx-x64`) differs. You can delete the second line in 3. If the name is `arc` already!

2.	Open the Terminal
e.g. hit command + spacebar and enter “Terminal”

3.	Execute in the terminal (copy each line or in block and execute):
```
cd Downloads
mv arc_osx-x64 arc
chmod a+x ./arc
mv ./arc /usr/local/bin/
```

4. Test installation

Execute in the terminal in any directory without the `arc` file:   
`arc --version`   

### Tested for Windows 10:

1.	Download the Windows version from [here](https://github.com/nfdi4plants/ARCCommander/releases): arc_win-x64.exe 

2.	Move this file into a directory of your choice (not an ARC), if you have already another version installed, place this file in the same directory. If both have the same name, replace the previous file with the new file.

3.	In the file explorer, go into the directory in which you placed the download and type “cmd” in the field showing the file path.

4.	The command prompt opens inside this directory  

5.	Now type the following and hit enter – this removes your previous arccommander installation if you have the respective file in this directory:   
`del arc.exe`   
   
6.	Now type the following and hit enter:
`ren arc_win-x64.exe arc.exe`  

7.	Now you have to add this file or the respective directory to your PATH. If you do not know how to do this, follow the instructions in the DataPLANT Knowledgebase: https://nfdi4plants.org/nfdi4plants.knowledgebase/docs/ArcCommanderManual/arc_installation_windows.html at point 3.  

8.	Test in another folder (repeat 3. & 4. inside another folder, e.g. an existing ARC)
Type the following and press enter:   
`arc --version`   


Optional: Check the DataPLANT KnowledgeBase for [installation instructions](https://nfdi4plants.org/nfdi4plants.knowledgebase/docs/ArcCommanderManual/).   


### Test current installation instructions for Linux:

1.	Download the Linux version from [here](https://github.com/nfdi4plants/ARCCommander/releases): arc_linux-x64 

2.	Open the Terminal

3.	Execute in the terminal (copy each line or in block and execute):
   
```
cd Downloads
mv arc_osx-x64 arc
chmod a+x ./arc
mv arc $HOME/bin/
```

4. Test installation

Execute in the terminal in any directory without the `arc` file:   
`arc --version`   

## ARCitect
ARCitect is not yet recommended (at the time point of the hackathon) but a good starting point to familiarize with the ARC.

Repository: https://github.com/nfdi4plants/ARCitect   
Knowledge Base: https://nfdi4plants.org/nfdi4plants.knowledgebase/docs/ARCitect-Manual/index.html  

## Swate

Repository: https://github.com/nfdi4plants/Swate   
Knowledge Base: https://nfdi4plants.org/nfdi4plants.knowledgebase/docs/SwateManual/index.html   

## Swate alpha

A Swate version for the browser: https://swate-alpha.nfdi4plants.org/   

## Additional links for specialists / the hackathon

### ARC specification
Last but not least: Link to [ARC specification](https://github.com/nfdi4plants/ARC-specification) - "New version (!), now also similar to [Grow-an-ARC](https://git.nfdi4plants.org/andreaschrader/Grow-an-ARC_Example) <-> [map-by-seq_CLSM-stacks](https://git.nfdi4plants.org/natural-variation-and-evolution/microscopy_collection/map-by-seq_clsm-stacks) providing examples along with how they understand an ARC."

### ARCtrl
Repository: https://github.com/nfdi4plants/ARCtrl  

### ARC validate
Repository: https://github.com/nfdi4plants/arc-validate  