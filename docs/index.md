# How to Convert a CSV File to a Shapefile

1. **Prepare Your CSV File**
   - Ensure your CSV file contains coordinate fields such as **Latitude/Longitude** or **X/Y** in projected units.
   - Confirm that the coordinate fields are clearly labeled (e.g., `Longitude`, `Latitude`, `X_Coord`, `Y_Coord`).
   - Save the file locally on your computer and close it in Excel before importing.

2. **Open ArcGIS Pro**
   - Launch ArcGIS Pro and either create a new project or open an existing one.

3. **Add the CSV File to Your Map**
   - In the **Catalog** pane or using the **Map** tab, click **Add Data** and browse to the location of your CSV file.
   - Add the file to your map. It will appear as a non-spatial table in the **Contents pane**.

4. **Display XY Data**
   - Right-click the table (CSV) in the Contents pane and select **Display XY Data**, or navigate to the **Map** tab and choose **Add XY Data**.
   - In the dialog that opens, assign the appropriate fields for the **X-coordinate** (e.g., `Longitude` or `X_Coord`) and **Y-coordinate** (e.g., `Latitude` or `Y_Coord`).

5. **Choose the Correct Coordinate System**
   - If your data uses geographic coordinates (latitude/longitude), choose **WGS 1984**.
   - If your data uses projected coordinates or is intended for mapping in Louisiana, select the local coordinate system:  
     **NAD 1983 (2011) StatePlane Louisiana South FIPS 1702 (US Feet)**  
     *(Well suited for South Louisiana projects such as transportation, utilities, and environmental mapping.)*

6. **Create the XY Event Layer**
   - Click **OK** to create a temporary event layer on the map based on your coordinate fields and chosen spatial reference.

7. **Export to Shapefile**
   - Right-click the new XY event layer in the Contents pane and choose **Data > Export Features**.
   - In the **Export Features** dialog:
     - Choose a destination folder.
     - Provide a meaningful name for your shapefile.
     - Confirm the output coordinate system matches your project needs (preferably Louisiana South).
   - Click **OK** to save the layer as a shapefile.

8. **Verify the Output**
   - The shapefile will now appear in your map as a permanent spatial layer.
   - Compare its placement against a known basemap (e.g., imagery or roads) to confirm spatial accuracy.

9. **Optional: Add Metadata or Join Attributes**
   - Use **ArcGIS Pro** tools to further enrich the shapefile with metadata, attribute joins, or symbology based on other columns in your CSV.
