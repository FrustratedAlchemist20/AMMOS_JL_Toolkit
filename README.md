# AMMOS_JL_Toolkit
Automated Massbank MS2 toolkit to Obtain Spectras

AMMOS: Automated Massbank MS2 toolkit to Obtain Spectras
========================================

Author
------
Sergio Pérez Tabero
Universidad Autónoma de Madrid (UAM)

Description
-----------
This project provides a Python/Jupyter-based toolkit for retrieving, processing,
and visualizing MS2 spectra from the MassBank database.

The program allows users to search MassBank records, load spectra from the
official MassBank data archive, extract peak lists, optionally assign fragment
formulas, and export the results into standardized `.dat` files.

In addition, the toolkit provides interactive spectrum visualization directly
within JupyterLab, allowing users to explore fragmentation patterns and inspect
spectral peaks dynamically.

The tool was designed to simplify the preparation and exploration of MS/MS
spectra for further analysis and computational workflows.


Main Features
-------------
- Search MassBank MS2 records by compound name
- Load MassBank records from the MassBank data archive (local or GitHub)
- Extract peak information from the `PK$PEAK` section
- Assign fragment formulas using `PK$ANNOTATION`
- Apply a ppm tolerance for formula matching
- Export spectra as `.dat` files
- Automatically generate a logbook (README) describing the exported spectra
- Interactive visualization of mass spectra
- Dynamic peak inspection with display of *m/z* and relative intensity
- Customizable spectrum filtering and plotting options

Requirements
------------
-> Python 3.8 or higher

-> Required Python packages:

-> numpy

-> IPython

-> pandas

-> ipywidgets

-> matplotlib

-> ploty

-> ipympl

-> mplcursors

-> requests



Install dependencies (Different options)
------------
A) Clone the repository:

$ git clone [https://github.com/USERNAME/massbank-ms2-extraction-toolkit.git](https://github.com/FrustratedAlchemist20/AMMOS_JL_Toolkit.git)

B) Move into the project folder:

$ cd AMMOS_JL_Toolkit

C) Install dependencies if needed:

$ pip install pandas [package]

D) With conda

$ conda install [package]

E) Using environment for conda from ammos-env.yml

conda env create -f ammos.yml
conda activate ammos-env

Usage
-----
1. Launch Jupyter Notebook or Jupyter Lab.

2. Open the notebook `AMMOS.ipynb`.

3. In the interface:

   - Enter a molecule name and press "Search MS2"
     OR

   - Paste MassBank accessions manually.

4. Select the spectra you want to process.

5. Set the ppm tolerance for formula matching.

6. Click "Load selected" to parse the spectra.

7. Click "Export .dat + README" to generate the output files.

The exported files will be written to the output directory
(default: massbank_dat).


Output
------
For each MassBank accession, the program creates a .dat file containing:

intensity    mz    formula

Where:

intensity  = relative intensity (%)
mz         = mass-to-charge ratio
formula    = fragment formula if available


In addition, a README log file is generated for each molecule containing
metadata about the spectra used (instrument, ion mode, collision energy, etc.).

## Interactive demo

This repository provides a toolkit for extracting and visualizing MS2 spectra from MassBank.

The toolkit includes:

- MassBank MS2 record extraction
- Interactive spectrum visualization
- Peak highlighting and annotation
- Export to .dat format

### Run online

You can run the notebook without installing anything:

[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/FrustratedAlchemist20/AMMOS_JL_Toolkit/HEAD?urlpath=lab)

Test
-----
In this folder you got two examples of tow dofeerent molecules Mass Spectra. 

Notes
-----
The tool reads spectra from the official MassBank data archive. If a local
copy of the archive is not provided, the program will download the archive
from GitHub automatically.


License
-------
This project is licensed under the MIT License - see the LICENSE file for details.


Citation
--------
If you use this tool in academic work, please cite:
FrustratedAlchemist20. (2026). FrustratedAlchemist20/AMMOS_JL_Toolkit: AMMOS JL Toolkit v1.0 (v1.0). Zenodo. https://doi.org/10.5281/zenodo.18882841
