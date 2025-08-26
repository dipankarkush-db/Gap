AI-Driven Table & Column Commenting Tool

This tool leverages the ai_query
 function to automate the generation and application of comments on tables and columns in Unity Catalog.

Overview

The solution consists of two main components:

Generator Notebook

Uses the ai_query function to generate comments for selected tables and columns within a schema in a catalog.

Saves the generated comments in JSON format to a Unity Catalog (UC) Volume.

Importer Notebook

Reads the generated comments from the UC Volume.

Applies the comments to the respective tables and columns in the catalog.

Structure

The example is provided as a DBC archive in this public Git repository.

There are four notebooks, organized into two sets, with each set containing a generator and an importer notebook.

Important Notes

This is a field-generated solution, tested for specific customer use cases.

Users should be aware that there may be potential issues or limitations in other environments.
