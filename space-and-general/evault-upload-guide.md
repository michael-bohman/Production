---
description: 'Owner: Isaac'
---

# EVault Upload Guide

This page is a guide for taking a model and creating the necessary files/drawings and uploading it all to EVault.

## Getting a Part Number

Navigate to the spreadsheet and find an open space, copy the few lines and input your things. Send this to wayne for approval.



## Creating a Drawing

### Notes:

#### Fonts

* small: height 0.08
* default: height 0.15625/0.14 (whatever is default)

#### Tools

* Text: Annotate>Annotations>Note>Unattached Note
* Inserting Model: Layout>Model Views>General View>Click to insert
* Projection View: Layout>Model Views> Projection View>Click on original>click above or beside to insert
* Add Dimension: Annotate>Annotations(drop down)>Reference Dimension>click on feature to dimension>MIDDLE CLICK to place text. a. for diameters, click on text>Orientation>Diameter

#### Other

This is for creating a new drawing for an all-new part, no complications like dashes or Revs



### Setup

#### Model Setup

1. Create an ISO view:&#x20;
   1. Orient model until an isometric view is achieved.
   2. View Manager (in hot bar with chart and camera)
   3. Orient>New
   4. Rename to ISO
2. Rename model number using 'manage file' to FULL part number, e.g. "25426-00\_REV-.prt"

#### Drawing Setup

1. Create New Drawing
2. name it part number, e.g. "25426"
3. select the correctly named part being used in the drawing
4. click 'empty with format'
5. Select the format (first page is fw\_format.frm.16, second is fw\_format2.frm.6)

### Creating the Drawing

#### Bottom Right Corner

DR: Your Name "J. SMITH" (default font)\
DATE: next to name in YYMMDD format (small font)\
TITLE: Part NAME, e.g. "JIG, IMU CALIBRATION, 65R" (default font)\
DRAWING NO: Should be set automatically to pt # e.g. "25426"

#### Top Right Corner

ZONE: Empty\
REV: "-"\
CHG NO: change to "N/A" (same font as already)\
APPD: Change to initials, e.g.. "JMS" (same font as already)\
DATE: Change to date, using same font and format (YYMMDD)\
DWG NO: Should be defaulted to the part number, e.g.. "25426"

#### Top Left Corner

Shouldn't have to change anything

#### Bottom Left Corner:

Add Notes Section Copy/Paste from a different drawing (like 25426).&#x20;

Changes:

1. Add single spaces between each numbered line
2. tab over the second and third lines (should be 3 spaces)
3. change TAG number to match drawing number

#### Center

1. Insert Model into drawing
2. Select ISO View
3. Open View Display Tab
   1. Display Style: No Hidden > Apply
   2. Tangent edges display style: Dimmed (or whatever looks best) > Apply
   3. Click 'Close'
4. Select model view > toggle OFF 'Lock View Movement'. Move upper right area
5. Under Isometric view, insert unattached note that says "ISOMETRIC REFERENCE VIEW" (Font \~0.2, whatever looks best)
6. Insert new view in bottom left area
   1. This will be projected, make it a view that will look good when it is projected.
   2. View Display settings, same as ISO view
7. Add projection view above previous
8. Click on new projection view, 'Edit Definition'.
   1. View Display settings, same as ISO view
9. Add projection view to the right of previously referenced view (should be placed in bottom right area)
10. Click on new projection view, 'Edit Definition'.
    1. View Display settings, same as ISO view
11. Move views around to make sure it is visually appealing
12. Add reference dimensions to views.
    1. Don't need very much, just a few general ones or any important dimensions
13. Export to PDF.
    1. go to file>save as>save a copy
    2. Select pdf.
    3. Add "\_rev-" to part number (e.g. "25426\_rev-").
    4. Click save.
    5. In options window:
       * select highest dpi (usually 600)
       * select 'monochrome'

## Compiling the files and Uploading

### Setting up the EVault folder

Create the folders:

* Part number - Part name (e.g. 25426 - Jig, IMU Calibration, 65R)
  * Archive
  * Rev-
    * natives

In the Rev- Folder:

1. Save the STP file
2. Save the drawing as pdf
3. maybe save STL file (if 3D printing regularly)

In the natives folder:

1. Save the backup THROUGH DRAWING
   1. This will include drawing, format, and part

