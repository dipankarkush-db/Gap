This tool uses the [ai_query] (https://learn.microsoft.com/en-us/azure/databricks/sql/language-manual/functions/ai_query) function.

There are two parts to it - Generator notebook and Importer notebook

The generator uses the ai_query function to generate the comments for the selected tables and columns in the schema within a catalog. The generated comments are saved in the Unity Catalog (UC) Volume in JSON format

The importer then reads the comments from the UC volume and applies the comments to the respective tables and columns

The example is loaded as a DBC archive in this public git repository

There are four notebooks, organized into two sets, with each set containing a generator and an importer.

This is a field-generated solution. Hence, we need to set the expectations that there could potentially be issues, as this is only tested for specific customer use cases.
