# AI-generated Table & Column Comment generation in bulk

This tool uses the [ai_query](https://learn.microsoft.com/en-us/azure/databricks/sql/language-manual/functions/ai_query) function to automate the generation and application of comments on tables and columns in Unity Catalog.

## Overview

The solution consists of **two main components**:

### Generator Notebook
- Generates comments for selected tables and columns in a schema within a catalog using `ai_query`.  
- Saves the generated comments in **JSON format** to a Unity Catalog (UC) Volume.

### Importer Notebook
- Reads comments from the UC Volume.  
- Applies the comments to the respective tables and columns.

## Structure

- Notebooks are organized in table and column sub folders
- Contains **four notebooks**, organized into **two sets**, one for table and the other one for column, each with a generator and an importer.

## Notes

- This is a **field-generated solution**, tested on specific customer use cases.  
- Potential issues may exist when used in other environments.
- This was tested using Databrciks Serverless notebooks
- Databricks foundation model serving endpoint - `databricks-meta-llama-3-3-70b-instruct` - was used for testing
- Databricks [Foundation Models](https://learn.microsoft.com/en-us/azure/databricks/machine-learning/model-serving/score-foundation-models#-foundation-model-types) have been used for this purpose. Users can compare different model-generated texts and decide on their choice of model-serving endpoint. They need to be mindful of the [supported regions](https://learn.microsoft.com/en-us/azure/databricks/machine-learning/model-serving/foundation-model-overview#-foundation-models-hosted-on-databricks) for the model serving endpoint.
