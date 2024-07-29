# photo-locating
Locate your photos using embedded exif metadata

Extract geodata from image files and plot a folium map with all accessions located within it.
A conda environment with `exifread`, `jupyter`, `ipykernel` and `pandas` installed is required. The utility was designed as jupyter notebook so one should use an IDE or browser to run the code.
___
Photos to be used as a source of exif data should be located at the `photos` directory. A table with all geoposition data extracted expected to be saved to the `output` directory that is automatically created.
A resulted map is plotted via [Folium](https://python-visualization.github.io/folium/latest/index.html) in the notebook cell output. To share the map one can use Google Collab sheets or save it to a file.

### How to use
As a first prerequisite, conda should be installed. The miniconda edition is ok for all purposes related to exif parsing and map plotting.
```bash
# if one wish to create an environment by their own
conda create -n geo-env python folium pandas jupyter ipykernel notebook exifread

# or if one wish to use a setup that is known to perform well.
# A yaml file from the repo might be used.
conda create --file=geo-env.yml
```
In the working location, create a `photos` directory and simlink/copy photos to be parsed to it.
Run the code in IDE (or in Collab, or in Jupyter-lab), executing cell-by-cell.
As an IDE, the VS Code with python and jupyter plugins installed might be used.
If one prefer to use a browser for notebook executing, an `ipykernel` could also launc the notebook by running `notebook` command in activated conda environment.
