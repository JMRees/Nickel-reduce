# Nickel-reduce
Data reduction for the Nickel CCD2 detector

# Requirements
Requires astropy>=5.3, numpy, scipy, matplotlib, astroquery, and astroscrappy.

An environment file is provided for those wanting to run these notebooks in a standalone conda environment. Add a new conda environment using: conda env create -f nickenv.yaml

# Process
Use nickel-calib to reduce your data files for a given night. This will de-bias and flatfield your data frames, as well as apply bad pixel maps and cosmic ray rejection. 

Use nickel-photom to perform aperture photometry on stellar sources, and match against an all-sky survey for photometric calibration. 

nickel-standards has the bare bones for determining photometric calibrations from standard star observations instead, which can then be applied to your instrumental magnitudes from nickel-photom.
