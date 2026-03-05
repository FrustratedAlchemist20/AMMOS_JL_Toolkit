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
This project provides a simple Python/Jupyter tool for retrieving and processing
MS2 spectra from the MassBank database.

The program allows users to search MassBank records, load spectra from the
official MassBank data archive, extract peak lists, optionally assign fragment
formulas, and export the results into standardized .dat files.

The tool was designed to simplify the preparation of MS/MS spectra for further
analysis and computational workflows.


Main Features
-------------
- Search MassBank MS2 records by compound name
- Load MassBank records from the MassBank data archive (local or GitHub)
- Extract peak information from the PK$PEAK section
- Assign fragment formulas using PK$ANNOTATION
- Apply a user-defined ppm tolerance for formula matching
- Export spectra as .dat files
- Automatically generate a logbook (README) describing the exported spectra


Requirements
------------
Python 3.8 or higher

Required Python packages:

pandas
ipywidgets
IPython


Installation
------------
Clone the repository:

git clone https://github.com/USERNAME/massbank-ms2-extraction-toolkit.git

Move into the project folder:

cd massbank-ms2-extraction-toolkit

Install dependencies if needed:

pip install pandas ipywidgets


Usage
-----
1. Launch Jupyter Notebook or Jupyter Lab.

2. Open the notebook that contains the MassBank toolkit.

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


Notes
-----
The tool reads spectra from the official MassBank data archive. If a local
copy of the archive is not provided, the program will download the archive
from GitHub automatically.


License
-------
MIT License


Citation
--------
If you use this tool in academic work, please cite:

Sergio Pérez Tabero
MassBank MS2 Spectrum Extraction Toolkit
Universidad Autónoma de Madrid
