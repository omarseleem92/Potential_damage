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


**The Python script performs the followingtasks:**
1. The script initially reads the water depth raster, which should adhere to specific criteria: it must be in 5-meter resolution, with water depth represented in centimeters, and it should share the same projection as the BEAM dataset. Once read, the script transforms the water depth raster into a polygon shapefile layer and subsequently dissolves it to obtain the boundary. Using the generated shapefile, the script then proceeds to clip the BEAM dataset accordingly.
2. Additionally, it creates a raster for each land use type found within the BEAM dataset. These rasters are saved in a designated folder named "Beam_rasters_clipped." Moreover, the script identifies and extracts fixed values based on the land use category code (ln_value). These fixed values are clipped and stored in a separate folder named "Fixed_values_rasters_clipped."
   ![image](https://github.com/omarseleem92/Potential_damage/assets/57235564/140261e8-bf70-4ed6-8eb7-26ac29088595)

4. The script proceeds to compute the potential damage for each land use type. This computation relies on the water depth data and utilizes predefined damage equations, which are outlined in the table below
   ![image](https://github.com/omarseleem92/Potential_damage/assets/57235564/161616a2-faff-448b-97c2-a803190d2558)

6. Finally, the Python script sums all the calculated damage from each land use and saves them in a raster named "Sum_damage.tif".

   ![image](https://github.com/omarseleem92/Potential_damage/assets/57235564/66058589-62dd-45cc-943e-df5d99346777)


## Example

The example folder contains a water depth file, the Python script, and the results obtained from running the script for a case study in Berlin. The figure below illustrates both the water depth and the calculated potential damage.

![image](https://github.com/omarseleem92/Potential_damage/assets/57235564/86995303-7f9e-4ecb-a6e8-b940e76a25c9)

## Reference
1.https://www.wasserblick.net/servlet/is/219256
2. https://www.wasserblick.net/servlet/is/219256/20220927_Empfehlung-PFRA-Anlage.pdf

