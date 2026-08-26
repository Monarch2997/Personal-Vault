###### First thing to do after opening Maya:
Top left tab swaps between
1. Modeling
2. Rigging
3. Animation
4. FX
5. Rendering
6. Customize
Switching changes what top bar options you have. Choose the tab that suits your current task

Key: Poly Modeling = shapes
*Also see create -> polygon primitives to see basic shapes*

Tools on the left are simply hotkeys for object manipulations (ex. r to rotate)

###### What does the window icon mean everywhere?
Many buttons have a window icon which when clicked brings up an options menu
*(ex. Polygon cube options menu lets you change the base state of cubes before you drop one into the viewport)*
###### On the right:
**Channel Box:**
Shows common attributes such as position, rotation, and translation. Visibility is also kept here
**Attribute Editor:**
Lets you change all of the small details of an object (ex. can change it to have LOD display so it loads more detail the closer you are and less detail the further)
**Modeling Toolkit**
Easy access to the most common tools. They are often also at the top of your screen. *(ex. insert edges)*

###### Top right corner
Dropdown that lets you swap between different types of workspaces. This changes your UI so that maya is more optimized for you task

###### Windows Top bar:
**Outliner**
Outliner is a separate tab that may be opened. This will list all objects. Its a simple overview of your scene

###### Views:
Perspective view is the base. Hold down alt to move the camera the right, left, and middle mouse buttons. This lets you rotate, pan, and zoom.

Press the spacebar to split the screen into 4 windows. Each is a new view that you can choose. Press spacebar again while your curser is over a panel to enter it

Icons also exist on the left side to change panel 

###### Component Mode:
To swap to component mode, hold down the right mouse button and select a tab within the wheel. 
1. Vertex is points on the object
2. Faces are sides
3. object mode is the full objects
4. Edge is a line between two vertexes

Hold down J to start snapping instead of full degree change

###### Creating more faces
Mesh Tools -> Insert Table loop
it creates a loop around your object which lets you move it around the object. Once you stop holding down left click, it creates a cut

Multi-cut is also in mesh tools. This lets you create cuts corner from corner.
###### Extrude
Extrude tool exists on the top bar. Control + E also works. Best example is to select a face, turn on the extract tool, and then you can change the scale of the new face you created. You can pull it in, out, and all about. Do NOT stack the extract tool. They will stack. It will be hell

###### Pivot Points
Press D to move the pivot point to a different vertex on your object. This allows for a very easy rotation

###### Merging objects:
Delete the faces that are going to collide and become unseen. Select the objects you are combining and then go to the Mesh tab and select the button combine. 

Select the opposing edges, then go to Edit Mesh and select Bridge. **Press G to repeat previous action**

###### Box Selection
In common selection options, you can set it to camera based selection. Alternatively, you can hold the tab key down and then select faces. Both of these prevent you from selecting unwanted faces when doing a large scale/box selection

###### Skeletons
Recommended to go to side view so you have a clearer view of the body where you are putting the bones in. Use the Rigging tab to create a few joints. Make joints where the bones end. 

Select the joints and attach the mesh to the bones. Go to the Skin tab and use bind skin. You can now select a joint and move it around.