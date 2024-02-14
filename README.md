# Potential_damage
Bund/Länder- Arbeitsgemeinschaft Wasser (LAWA-AH) decided to conduct the preliminary assessment starting from the 3rd cycle of implementation of the EU Flood Risk Management Directive based on a nationwide dataset of damage potential and a unified methodology for damage potential calculation.This repository computes potential damage using the BEAM dataset. This repository computes potential damage using the BEAM dataset. More information about the BEAM dataset https://www.wasserblick.net/servlet/is/219256/

## Installation Guide for Required Python Packages

To run the Python script successfully, ensure that you have installed the following Python packages:

1. **rasterio**: Provides functionality for reading and writing geospatial raster data.
    ```
    pip install rasterio
    ```

2. **geopandas**: Extends the datatypes used by pandas to allow spatial operations on geometric types.
    ```
    pip install geopandas
    ```

3. **shapely**: Manipulates and analyzes geometric objects in the Cartesian plane.
    ```
    pip install shapely
    ```

4. **fiona**: Reads and writes geographic data files (both vector and raster formats) using Python code.
    ```
    pip install fiona
    ```

5. **geocube**: Creates data cubes from raster data and allows for easy conversion between raster and vector data.
    ```
    pip install geocube
    ```

6. **numpy**: Provides support for large, multi-dimensional arrays and matrices, along with a large collection of mathematical functions to operate on these arrays.
    ```
    pip install numpy
    ```


7. **glob**: Allows for pathname pattern expansion.
    ```
    pip install glob
    ```

8. **os**: Provides a way of using operating system-dependent functionality.
    ```
    pip install os
    ```

9. **shutil**: Offers high-level operations on files and collections of files.
    ```
    pip install shutil
    ```

10. **time**: Provides various time-related functions.

Please ensure that you have installed the required packages before running the Python script. You can install these packages using pip, a package management system for installing and managing Python packages. After installing the packages, you should be able to execute the script without any issues.




## Required Input data for Script Execution

To successfully execute the Python script, you need to provide the following input parameters:

1. **WD_raster_file**: This parameter specifies the path to the waterdepth raster file. Please ensure that you provide the full path to the raster file, including the file extension (e.g., `.tif`).It must be in 5-meter resolution, with water depth represented in centimeters, and it should share the same projection as the BEAM dataset (EPSG: 3035).
2. **BEAM_file**: This parameter indicates the path to the BEAM dataset. Ensure that you provide the full path to the BEAM dataset directory or file.
3. %3CmxGraphModel%3E%3Croot%3E%3CmxCell%20id%3D%220%22%2F%3E%3CmxCell%20id%3D%221%22%20parent%3D%220%22%2F%3E%3CmxCell%20id%3D%222%22%20style%3D%22edgeStyle%3DorthogonalEdgeStyle%3Brounded%3D0%3BorthogonalLoop%3D1%3BjettySize%3Dauto%3Bhtml%3D1%3BentryX%3D0.5%3BentryY%3D0%3BentryDx%3D0%3BentryDy%3D0%3B%22%20edge%3D%221%22%20source%3D%223%22%20target%3D%227%22%20parent%3D%221%22%3E%3CmxGeometry%20relative%3D%221%22%20as%3D%22geometry%22%2F%3E%3C%2FmxCell%3E%3CmxCell%20id%3D%223%22%20value%3D%22BEAM%26lt%3Bbr%26gt%3Bdataset%22%20style%3D%22whiteSpace%3Dwrap%3Bhtml%3D1%3Baspect%3Dfixed%3B%22%20vertex%3D%221%22%20parent%3D%221%22%3E%3CmxGeometry%20x%3D%22130%22%20y%3D%22220%22%20width%3D%2280%22%20height%3D%2280%22%20as%3D%22geometry%22%2F%3E%3C%2FmxCell%3E%3CmxCell%20id%3D%224%22%20style%3D%22edgeStyle%3DorthogonalEdgeStyle%3Brounded%3D0%3BorthogonalLoop%3D1%3BjettySize%3Dauto%3Bhtml%3D1%3B%22%20edge%3D%221%22%20source%3D%225%22%20target%3D%227%22%20parent%3D%221%22%3E%3CmxGeometry%20relative%3D%221%22%20as%3D%22geometry%22%2F%3E%3C%2FmxCell%3E%3CmxCell%20id%3D%225%22%20value%3D%22Water%20depth%22%20style%3D%22whiteSpace%3Dwrap%3Bhtml%3D1%3Baspect%3Dfixed%3B%22%20vertex%3D%221%22%20parent%3D%221%22%3E%3CmxGeometry%20x%3D%22240%22%20y%3D%22220%22%20width%3D%2280%22%20height%3D%2280%22%20as%3D%22geometry%22%2F%3E%3C%2FmxCell%3E%3CmxCell%20id%3D%226%22%20value%3D%22%22%20style%3D%22edgeStyle%3DorthogonalEdgeStyle%3Brounded%3D0%3BorthogonalLoop%3D1%3BjettySize%3Dauto%3Bhtml%3D1%3B%22%20edge%3D%221%22%20source%3D%227%22%20target%3D%228%22%20parent%3D%221%22%3E%3CmxGeometry%20relative%3D%221%22%20as%3D%22geometry%22%2F%3E%3C%2FmxCell%3E%3CmxCell%20id%3D%227%22%20value%3D%22Python%20script%22%20style%3D%22ellipse%3BwhiteSpace%3Dwrap%3Bhtml%3D1%3B%22%20vertex%3D%221%22%20parent%3D%221%22%3E%3CmxGeometry%20x%3D%22160%22%20y%3D%22330%22%20width%3D%22120%22%20height%3D%2280%22%20as%3D%22geometry%22%2F%3E%3C%2FmxCell%3E%3CmxCell%20id%3D%228%22%20value%3D%22Potential%20Damage%20(EUR)%22%20style%3D%22whiteSpace%3Dwrap%3Bhtml%3D1%3Baspect%3Dfixed%3B%22%20vertex%3D%221%22%20parent%3D%221%22%3E%3CmxGeometry%20x%3D%22180%22%20y%3D%22440%22%20width%3D%2280%22%20height%3D%2280%22%20as%3D%22geometry%22%2F%3E%3C%2FmxCell%3E%3C%2Froot%3E%3C%2FmxGraphModel%3E

## Example

The example folder contains a water depth file, the Python script, and the results obtained from running the script for a case study in Berlin. The figure below illustrates both the water depth and the calculated potential damage.

![image](https://github.com/omarseleem92/Potential_damage/assets/57235564/86995303-7f9e-4ecb-a6e8-b940e76a25c9)


