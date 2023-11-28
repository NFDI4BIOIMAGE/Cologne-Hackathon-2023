# Installation and instructions

:construction: Under construction! :construction:

Notes to consider when providing installation instruction and other helpful links
- point to the DataPLANT KnowledgeBase
- git
- git-lfs
- ARCcommander - suggest preview2 for v1.0.0
(- ARCitect - not yet recommended)
- Swate
- Swate alpha
- register at HUB
- create an ARC (either in the HUB with a template or locally)
- sync once an ARC with the HUB - do not worry about failing pipelines - arc validation is under constructions
- add at least one building block using Swate
- Grow-an-ARC - example for filling the isa.investigation file using ARCcommander v0.5.0
- A simple microscopy ARC in the making and used as a template for Grow-an-ARC
- hint to ARC specification - "New version (!), now also similar as Grow-an-ARC providing examples along with how they understand an ARC."
- hint to ARCtrl Python version under development

## DataPLANT HUB (GitLab)
Please [**sign up**](https://auth.nfdi4plants.org/realms/dataplant/login-actions/registration?client_id=gitlab-fr&tab_id=ie6dwnHi6Uc) for access to the DataPLANT HUB!

## Installing the suggested **(preview) version of the ARCcommander**

### Requirements (ARC Commander)
**git**  
**git-lfs**  

Installing a (preview) version of the ARCcommander for experienced users (just execute the code block in 3. And check the name of the version you want to install) and with more detailed comments for beginners:

Add the link https://github.com/nfdi4plants/ARCCommander/releases

Remove the old ARC commander version if not in `/usr/local/bin/` and not present somewhere else on the system.

You can also visit the [DataPLANT KnowledgeBase](https://nfdi4plants.org/nfdi4plants.knowledgebase). As it might repeatedly re-structured, some links might be dead after a while provided below. In such a case, the content, likely, will just have been moved within the KnowledgeBase.

### Tested for macOS 14.1.1 with Intel chip:

1.	Download the x64 version from [here](https://github.com/nfdi4plants/ARCCommander/releases) into the Download directory: arc_osx-x64 
You have to adjust accordingly the second line in point 3 below in case the name name of the downloaded file (here `arc_osx-x64`) differs. You can delete the second line in 3. If the name is `arc` already!

2.	Open the Terminal
e.g. hit command + spacebar and enter “Terminal”

3.	Execute in the terminal (copy each line or in block and execute):
cd Downloads
mv arc_osx-x64 arc
chmod a+x ./arc
mv ./arc /usr/local/bin/

4. Test installation

execute in the terminal in any directory without the `arc`` file.

### Tested for Windows 10:

1.	Download the Windows version from [here](https://github.com/nfdi4plants/ARCCommander/releases): arc_win-x64.exe 

2.	Move this file into a directory of your choice (not an ARC), if you have already another version installed, place this file in the same directory. If both have the same name, replace the previous file with the new file.

3.	In the file explorer, go into the directory in which you placed the arc download and type “cmd” in the field showing the file path.

4.	The command prompt opens inside this directory

5.	Now type the following and hit enter – this removes your previous arccommander installation if you have the respective file in this directory:
del arc.exe

6.	Now type the following and hit enter:
ren arc_win-x64.exe arc.exe

7.	Now you have to add this file or the respective directory to your PATH. If you do not know how to do this, follow the instructions in the DataPLANT Knowledgebase: https://nfdi4plants.org/nfdi4plants.knowledgebase/docs/ArcCommanderManual/arc_installation_windows.html at point 3.

8.	Test in another folder (repeat 3. & 4. inside another folder, e.g. an existing ARC)
Type the following and press enter:
arc --version


Optional: Check the DataPLANT KnowledgeBase for [installation instructions](https://nfdi4plants.org/nfdi4plants.knowledgebase/docs/ArcCommanderManual/).


### Test current installation instructions for Linux:
tbc



## ARCitect



## Swate



## Swate alpha



## ARC specification



## ARC control