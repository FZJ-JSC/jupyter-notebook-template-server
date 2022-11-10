# Jupyter notebook template server
Notebook templates offered by [Jupyter-JSC](https://jupyter-jsc.fz-juelich.de) to use with [SampleDB](https://scientific-it-systems.iffgit.fz-juelich.de/SampleDB/).  
  
Create a notebook, filled with parameters defined by a simulation in SampleDB, in your JupyterLab started by Jupyter-JSC.  

## Usage
1. Log in at https://jupyter-jsc.fz-juelich.de
2. Start a JupyterLab on any system
3. Choose a simulation in SampleDB and click on the "Create Notebook" button.
4. You will be redirected to Jupyter-JSC. Choose a running JupyterLab.
5. You will be redirected to the newly created Notebook.
  
## SampleDB configuration
To add Jupyter-JSC to any SampleDB instance add these environment variables:  
```
SAMPLEDB_JUPYTERHUB_NAME=Jupyter-JSC
SAMPLEDB_JUPYTERHUB_TEMPLATES_URL=https://jupyter-jsc.fz-juelich.de/hub/templates
```

For more information look into SampleDB [documentation](https://scientific-it-systems.iffgit.fz-juelich.de/SampleDB/administrator_guide/jupyterhub_support.html).

## Template features
### Insert parameter cell
Inserts a cell at the top of the notebook, where all configured parameters will be defined.  
Configuration in notebook:  
```
{
  "metadata": {
    "insert_parameter_cell": true
  }
}
```
Default: true

### Replace in all cells
Replace parameter key with given values in all notebook cells.  
Configuration in notebook:  
```
{
  "metadata": {
    "replace_in_all_cells": true,
    "replace_indicators": [
      "<<", ">>"
    ]
  }
}
```
Default: `replace_in_all_cells`: `false` , `replace_indicators`: `["<<", ">>"]`


