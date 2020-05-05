### This code is associated with the paper from Harman et al., "Evolution of multifunctionality through a pleiotropic substitution in the innate immune protein S100A9". eLife, 2020. http://dx.doi.org/10.7554/eLife.54100

Simple band quantification software for protein and DNA gels/blots. Takes an input image which gets cropped by the user. Then splits image into user-specified vertical lanes, which are temporarily saved. These lanes are then converted to numpy arrays, and the average RGB intensity of each row in the image slice is calculated. Intensities are gaussian-weighted so that the middle of the lane contributes more to the average than the outer edges, as other lanes sometimes bleed into the lane of interest. Data for each slice is baselined given a user-specified baselining region. This data is plotted and can be quantified for band intensities.

See notebook-example.ipynb and gel-example.png for details/example usage.

To install a development version, clone this repo and pip install:

pip install -e .

Dependencies: matplotlib, numpy, PIL, pandas, os, natsort, scipy
