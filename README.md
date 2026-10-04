# Bangkalan Sawah Classification

Student: Joni Kumar Meghwar
NIM: 240411100234
Location: Bangkalan, Madura, East Java, Indonesia

This version uses NO Google Earth Engine.

Workflow:
Copernicus Browser -> Sentinel-2 L2A TIFFs -> local Python/Rasterio -> Random Forest -> accuracy/Kappa/confusion matrix -> final GeoTIFF.

Required input files:
1. Browser_images.zip containing B02, B03, B04, B08, B11, B12 TIFFs.
2. sawah.zip containing a shapefile with a `class` field. The field must contain `sawah` and `bukan sawah`.

Download imagery from:
https://browser.dataspace.copernicus.eu/

The training polygons must be for the same Bangkalan study area as the Sentinel-2 imagery. The script does not invent or relocate old training polygons.

Run the Python script in Google Colab or locally. It will automatically stack/resample the six bands to the B02 grid.
