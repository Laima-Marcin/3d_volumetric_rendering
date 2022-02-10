# 3d_volumetric_rendering
3D volumetric rendering - scan of the head

In this exercise we use two methods of visualizing 3D medical volume of the head scan:

•	**Orthographic projection** – we sum up the intensities on all the slices, store the result in the variable and visualize it
This method of volume rendering is rather basic because while it does present all the information from a volume in a single image, it does not really make use of all the colours available to the display, it does not make distinction between tissue types.

•	**Maximum intensity projection** – we use np.maximum function to save the maximum value of each pixel across our entire slice stack.
This method makes sure that maximum values (in case of CT corresponding to the densest structures) are propagated and prominently visualized. 
A MIP projection can help a physician visualize foreign materials, bones or structures filled with a contrast medium.


NIFTI file with a CT volume is loaded into numpy array.
img_np is a numpy 3D array that contains our medical volume, its size is 360 x 360 x 330.
- The first dimension is the X axis, and if we slice the array across it, we will get slices in sagittal plane. 
- The second dimension is the Y axis, and slicing across it will get us the coronal plane. 
- Third dimension is the Z axis and if we slice across it we will get the axial plane. 
