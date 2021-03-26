# VHACD-for-MuJoCo
Convex decomposition approach for collision check on non-convex objects in MuJoCo

## System Descriptions
   Ubuntu 16.04

   Nvidia-GTX 1060

   Blender 2.78

## Prerequisites
   ### Install the V-HACD library for convex decomposition on the meshes.
  1. Clone [this Github repository](https://github.com/kmammou/v-hacd.git)
  2. Rebuild the binaries: running ```python run.py --cmake``` in the install directory, and then running make in the created build/linux directory
  3. Copy the Python script in ```v-hacd/add-ons/blender/object_vhacd.py``` to your Blender addons directory.  For Blender 2.78 this directory will be ```"Blender Foundation/Blender/2.78/scripts/addons/"```.  You're at the right place if you see other scripts prefixed with object\_.
  4. The addon must be enabled before use.  After copying the script to the addons directory, open Blender and navigate to File > User Preferences > Add-ons.  Object: V-HACD will be featured on the list.  Check its mark to enable the addon and save user settings.

  ### Using the Addon
   1. After you have enabled the addon, the V-HACD menu will appear in the object menu when an object is selected.
   1. Go to this menu and select a preset (or leave the path presets).
   1. Select your VHACD path by selecting the "Open File" button next to the VHACD path, which should currently be blank.
   1. Navigate to the directory in which you cloned this repository and find the appropriate executable in the bin folder for your operating systme.
   1. If you have a video card that supports OpenCL, this will be bin.
   1. If you don't have a video card or your video card does not support OpenCL, the appropriate executable for you will be bin-no-ocl (no OpenCL).
   1. Select the V-HACD button at the button of the panel.  You will be presented with some options.
   1. Modify the options as desired and select "OK."
   1. Note that the processing may take some time.  Increasing voxel resolution will particularly increase runtime.


## Running Convex Decomposition
The rebuilt binaries can be found at ```v-hacd/build/linux/test/testVHCAD```
Run ```$./testVHACD``` to look at decomposition options


   
