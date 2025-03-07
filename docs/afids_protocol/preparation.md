---
title: "AFIDS Protocol"
template: overrides/main.html
---

## Preparation

### 3D Slicer

Download and use 3D Slicer 4.10.2 (for the time being **DO NOT** use version 4.11 or above):

* **Windows (x64), Mac OS X, and Linux:** https://slicer-packages.kitware.com/#collection/5f4474d0e1d8c75dfc70547e/folder/60add36eae4540bf6a89be73

### Image Templates

Download template files:

<div id="tree"></div>
<script>
    $(document).ready(function() {
      $.ajax({
          url : "../assets/all_templates.json",
          dataType: "text",
          success : function (tree) {
              $('#tree').bstreeview({ data: tree });
          }
      });
});
</script>

## Naming Scheme for Fiducial Files

* [VolumeID]\_[Contrast]\_[Rater]\_[N] [e.g. macaqueMNI_T1_JL_01]

  * **[VolumeID]** = the identifier for the volume on which you are performing the fiducial placements (use the **name** given to the template in table above)
  * **[Contrast]** = T1 (all templates are T1)
  * **[Rater]** = the unique identifier for the rater performing the fiducial placement; convention will be first initial and last name to prevent overlap
  * **[N]** = reference for fiducial placement session (helpful if performing placements more than once; starting with 1)

## General Fiducial Placement Strategies

Use the **"Jump to Slice"** feature to center your view on the fiducial of interest and ensure that the placed landmark appears accurate 
on all three standard views (axial, sagittal, coronal). Once a fiducial is placed, **dragging** the fiducial can allow for more refined 
placement. Holding down **shift** centers the view in all views on the cursor (use along with crosshair function). If a given fiducial 
is classified as **[midline]**, jump to an existing midline fiducial (e.g. AC or PC) and start by placing the fiducial on the 
**sagittal** view and refine placement using the other views. Try to place fiducials at the **boundary/edge** of the feature of 
interest. For some of the fiducials, the instructions for placement will explicitly say to place the landmark using information mostly 
from one view (e.g. axial view for olfactory sulcus). Be aware that changing the windowing of your images (and lighting in the room) may 
affect your perception of where landmarks should be placed. When you're satisfied with the location of a fiducial, **lock it in place** 
to prevent yourself from displacing it later. **NOTE: there is no UNDO feature for fiducial placements.**

## Placement of Fiducial Series

Copy points from the **ACPC** markups list to the **Fid32\_[VolumeID]\_[Contrast]\_[Rater]\_[N]** markups list. Copy over AC and PC to your **Fid32** markups list by right clicking each fiducial, choosing "Copy fiducial to another list", and selecting **Fid32\_[VolumeID]\_[Contrast]\_[Rater]\_[N]**. Place the remaining **30 fiducials**, enter the number corresponding to the fiducial in the **Name** textbox and enter the description in the corresponding **Description** textbox. When placing the fiducials make sure you are on the **Fid32\_[VolumeID]\_[Contrast]\_[Rater]\_[N]** markup list.

To help with monitoring the current location of the pointer, toggle on the **Slice intersection** under **Toggle crosshair visibility**.

## Anatomical Direction Guide

### Human Anatomy

<p align="center"><img src="../img/human/anatomical_directions_human.png" alt="anatomical_directions" width="100%"/></p>

### NHP Anatomy

<p align="center"><img src="../img/nhp/anatomical_directions_nhp.png" alt="anatomical_directions" width="100%"/></p>

## AFIDs Validator

Once you have completed the placement of AFIDs, you are able to validate your accuracy by uploading the `.fcsv` file to the <a href="https://validator.afids.io/" target="_blank">AFIDs validator website</a>.

<br>
<br>
