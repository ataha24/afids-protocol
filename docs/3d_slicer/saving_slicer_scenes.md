---
title: "Saving Slicer Scenes"
template: overrides/main.html
---

!!! warning
	Ensure you are using **3D Slicer 4.10.2:**<br>
    **Windows (x64):** http://slicer.kitware.com/midas3/item/433684<br>
    **Mac OS X:** http://slicer.kitware.com/midas3/item/433773<br>
    **Linux:** http://slicer.kitware.com/midas3/item/435293<br>

## Walkthrough

1. Click on the **File** menu at the top.

	<p align="center"><img src="../img/fileMenu.png" alt="fileMenu"/></p>
	
2. Choose **Save**, the dialog box shown below will appear:

	<p align="center"><img src="../img/saveMenu.png" alt="saveMenu"/></p>

3. If this is your first time saving you will have to define the directory to save the files. Click on **Change directory for selected files**. The dialog box below will appear:

	<p align="center"><img src="../img/saveDir.png" alt="saveDir"/></p>


4. Find the directory where you want to save the data, create a new folder called **[VolumeID]\_scene** and then double click on it so you are now within the directory. Select **Choose**.

5. You will now notice that the **.nii** file is de-selected and is in the original directory location. All the other files you will be saving are in the newly created **[VolumeID]\_scene** folder. Click **Save**.

	<p align="center"><img src="../img/saveDir2.png" alt="saveDir2"/></p>

6. If this not your first time saving you will see two warning messages. The first will notify you that the **.mrml** file already exists and ask if you want to replace it. Click **OK**.

	<p align="center"><img src="../img/mrmlSave.png" alt="mrmlSave"/></p>

7. A second warning message will appear letting you know that the **.fcsv** file already exists and ask if you would like to replace it. Click **Yes to All**. This will overwrite your old datafiles with the newer ones.

	<p align="center"><img src="../img/fcsvSave.png" alt="fcsvSave"/></p>
	
8.	To close the current scene, before opening a new subject, click the **File** menu and select **Close Scene**.

	<p align="center"><img src="../img/closeScene.png" alt="closeScene"/></p>
