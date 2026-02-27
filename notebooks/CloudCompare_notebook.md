## 1. Opening files with CloudCompare

1. Download the individual_pointclouds folder from the OneDrive (ARS_TLS_course>data>individual_pointclouds) as a zip file and store it on your local PC.

#### Option 1: Open CloudCompare and click the <span style="color:red">file icon</span> in the top left of the window. Select all raycloud_segmented pointcloud files within the individual_pointclouds folder stored on your local PC. 

![Open File](./images/cc1.png)  

#### Option 2: Open CloudCompare, drag and drop the pointcloud files into the CloudCompare viewer window.

### 1.1 Open file settings
Depending on the file type, there are different options when opening a file. The options taken may vary depening on your projects' need. However in general it is usually best to **preserve as many fields as possible** and to select <span style="color:red">no</span> when shifting/scaling the data.

Load in standard fields for Ply files. Click on <span style="color:red">Apply all</span>:

![alt text](image.png)

## 2. CloudCompare main overview
Now that we have some data loaded, lets take a step back and examine the different parts of the interface.

![alt text](image-3.png)

The <span style="color:blue">blue box</span> highlights the toolbar with many important functions such as save, load, segment, merge, etc.

The <span style="color:yellow">yellow box</span> highlights the main viewing area. This is where we will manipulate and view our point clouds.

The <span style="color:green">green box</span> highlights our loaded files in a tree. Try toggling on/off some of the loaded data to get a sense of how it works.

The <span style="color:red">red box</span> highlights the properties for a selected point cloud. Note that this is point clouds specific. Also, using the mouse wheel while hovering over a drop down menu will change the options!

The <span style="color:pink">pink box</span> is the console. For now, it is only important to know that it will display some messages to help us stay informed.

## 3. Visualization basics
Before we manipulate data, we can make our lives easier by visualizing the data in our preferred manner. This is up to personal taste, so here we will supply an explanation of the basic options. For a more complex (and beautiful) visualization procedure, please read the color-tree-point-cloud-with-CloudCompare repository on the Q-ForestLab Github.

### 3.1 File unique colorization
When segmenting individual trees, it can be nice to assign each tree (and the remainder point cloud) specific colors. We can accomplish this in a few steps:
#### 1. Make sure to have the desired file selected
#### 2. Navigate to Edit > Colors > Set unique

![set unique](./images/5_cc_colorization_unique.png)

#### 3. Select the desired color

If you find yourself returning to the same colors, you can click 'Add to Custom Colors' to make them easily accesible in the future.

![set unique 2](./images/6_cc_colorization_unique_selection.png)

Then your tree will look like this.
![alt text](image-4.png)

### 3.2 Scalar field colorization (height gradient)
If you prefer to have some of your point clouds colored by height, this is a good option. You can also change the colors in the gradient.

#### 1. Navigate to Tools > Projection > Export coordinate(s) to SF(s)

![export coordinates to sfs](./images/7_cc_colorization_scalar_field.png)

#### 2. Export the desired coordinates to a scalar field
Assuming the point cloud is oriented with z pointing up, the z coordinate scalar field can be used for a height gradient.

![export coordinates to sfs 2](./images/8_cc_colorization_scalar_field_2.png)

Then your tree will look like this.
![alt text](image-5.png)

### 3.3 Miscellaneous visualization options
Lets take a closer look at some useful parts of the properties window:

![visualization properties](./images/9_cc_colorization_properties.png)

The <span style="color:yellow">yellow box</span> contains the options for toggling point cloud visibility, as well an option to switch between RGB (file unique colorization) and scalar field colorization (height gradient). There is also a toggle to display the point cloud label in the viewing window.

The <span style="color:green">green box</span> is a useful option to change point size. This is purely visual and does not modify the data. The points will display poorly on certain displays, and increasing the point size can help alleviate this.

The <span style="color:red">red box</span> contains the options to modify the color scale used in the scalar field colorization.

The <span style="color:blue">blue box</span> contains some options that will alter the display window, such as automatic selection of a camera rotation point, or snapping the view to the x, y, or z plane.

### Lastly, if you are interested in creating a crown map to help keep track of your segmentation progress, as well as have a list of the nearest neighboring trees for corrections, check out get_crown_shape.Rmd found in the scripts secion in this repo.

### That covers the basics of opening and visualizing files needed for segmentation, now you are ready to start segmenting!

## 4. Final preparation
Before segmenting, be sure to have your files visualized clearly. If you are following along with the demo data, you can see an example below:

![alt text](image-1.png)

## 5. Start Segmentation

We will focus on disentangling the demo tree 24 shown in <span style="color:orange">orange</span> from its neighbouring trees (21, 25, 26).

![alt text](image-7.png)

The overlapping part of the trees is highlighted in the above image in the <span style="color:pink">pink</span> box.

Before starting segmentation, ensure you have the correct file selected. Select the file for tree 1_1_23 (highlighted in the above image in the <span style="color:red">red</span> box)

Finally, we can start segmenting by clicking on the scissors icon, highlighted in the <span style="color:green">green</span> box, which will bring up the below toolbar:

![segmentation start](./images/12_cc_segment_options.png)

In the above image:
1. The <span style="color:red">red</span> box highlights the pause button. This button toggles drawing a polygon to select points/moving the viewing window. The hotkey is spacebar, although it is prone to malfunction.
2. The <span style="color:green">green</span> box will allow you to change between polygonal and rectangular selection.
3. The <span style="color:blue">blue</span> box highlights the segment in/segment out buttons. This will allow you to either hide points within a drawn polygon, or only display those points.
4. The <span style="color:pink">pink</span> box is an undo option.
5. The <span style="color:orange">orange</span> box opens a dialogue to change the automatic naming convention of segmented parts.
6. The <span style="color:yellow">yellow</span> box highlights the buttons to finish segmentation. This can be either by confirming the segmentation or cancelling. **WARNING** closing the segmentation session will eliminate all segmentation work completed since the last segmentation confirmation. The only way to segment is to select 'confirm segmentation,' and until then all progress is temporary. CloudCompare can be prone to crashing, so it is recommended to do this regularly.

Note that while a segmentation session is active, the other tools in the top toolbar are disabled. Therefore, if you want to increase the pointsize of the individual pointclouds to better cut out your demo tree, increase the point clouds before clicking the scissors icon as shown in the <span style="color:orange">orange scare</span> in the image below.

## 6. Polygon drawing and confirming segmentation

Now that we have segmentation started, we can zoom in to the overlapping area between the two demo trees and draw a polygon around the area we want to remove from tree 24. If you are unable to move the view window and are instead drawing a polygon, try pausing the segmentation as outlined in the previous step.

![alt text](image-8.png)

With a polygon drawn around the desired area, you can now click the 'segment out' button highlighted in the above image in <span style="color:red">red</span> to hide those points. Note that those points are not deleted, only temporarily hidden until we confirm segmentation. If you are unable to segment out points from tree 24, make sure it was selected in the file selection window before starting the segmentation tool.

When you are happy with the segmented out points, continue by clicking on 'confirm segmentation,' highlighted in the above image in <span style="color:green">green</span>. This will create a new segmented file in the file selection window (as seen in the figure below), and all the hidden points should reapper in the viewing window. To get a sense of how the new files are named, try turning selecting/unselecting them in the file selection window a few times. Congratulations, you've segmented a piece of a point cloud!

![alt text](image-9.png)

## 7. Merging files

We will now merge the segmented file from tree 24 into tree 26. Start by selecting both files in the file selection window (this can be done with ctrl + click).

**WARNING** The name of the newly created file after the merge will be based on the first file selected when selecting multiple files. File names can always be changed later, but creating continuity of file names can help in staying organized within a project.

With both files selected, click on the merge button (highlighted in the below image in <span style="color:red">red</span>). You can choose to create scalar fields if desired; this creates a new data field that will keep track of what point cloud individual pieces of the newly created combined point cloud originate from. It is not required but can be interesting for keeping track of segmentation progress in the future.

![alt text](image-10.png)

After your merge is complete, you can visualize the changes. You may need to recolor the newly combined point cloud if you chose to create a new scalar field. For the demo data, we are now left with the below image:

![alt text](image-11.png)

This covers the basic method of segmentation/merging that is required to reorganize point cloud data. Continue to do these steps until tree 24 is fully segmented and seperate from its neighbour trees.

## 8. Trees outside of the plot may interfere with individual tree pointcloud segmentation

Sometimes branches from a tree outside the scanned pointcloud is part of a segmented tree. this is the case of tree 24, meaning that these branches have to be removed from the pointcloud of tree 24 and added to the left over pointcloud, being in our case, pointcloud -1.

![alt text](image-12.png)

## 9. Segment the entirety of the tree trunk

It is important to verify if the entirety of the tree trunk is included within an individual tree pointcloud. Often a part of the trunk is still part of the left over pointcloud as shown in the <span style="color:pink">pink</span> polygon for tree 24 in the image below. 

![alt text](image-13.png)

Add the selected trunk to your tree pointcloud from a top view and add it to the segmented pointcloud of tree 24 following the segmentation guidelines above.

![alt text](image-15.png)

## 10. Saving data

None of this work is permanent until the files are resaved. 

Select the desired point cloud in the file selection window, then navigate to File > Save
![alt text](image-17.png)

Find the desired folder to save your point cloud in on your local PC. Then create a folder corrected_tree in the data folder on your google drive and upload your corrected tree file in that Onedrive folder. Pay careful attention to the naming/file type. If you make a mistake, later you can reopen your saved point cloud and save it as a different file type.

![alt text](image-18.png)

## Now that you have saved your freshly segmented tree, it's just a matter of repeating the process and staying organized. Good luck!


