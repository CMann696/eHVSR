# eHVSR
eHVSR from strong motion instruments

Horizontal to Vertical Spectral Ratios (HVSR) help identify fundamental frequencies of soil, and can estimate site amplification effects. Microtremor HVSR (mHVSR), often used in engineering practices, utilizes Earth's low-level background noise to study these site effects. However, in regions with enough active seismicity, earthquake waveforms can be used instead (eHVSR) to estimate site amplification. When H/V values are close to 1, wave amplification is minimal and the site is thought to be located at, or near bedrock. H/V values increase as the sedimentary surface layer depth increases, and results in increased wave amplification. HVSR studies are important to our understanding of how local infrastructure will respond to large earthquakes.

A comparison study was performed to determine if the use of strong motion instruments was reliably comparable to broadband instruments in earthquake HVSR. Findings indicated that for events < M4.0, results were very similar, except for events recorded on stations in close proximty to the event. Larger events have not been studied at this time. 

The following code is a work in progress, but streamlines the eHVSR process using strong motion instruments.
The provided "Download Waveforms" code will need to be adjusted if you wish to use broadband instruments instead of strong motion. It is recommended that stations with fewer than 10 events recorded not be used in eHVSR (Wang et al. 2023), as each event will serve as a window.

The order of functions in the process are as follows:
1) Search_Parameters
2) Gather Station Inventory
3) Extract Event Information
4) Make Metadata DataFrame
5) Download Waveforms (Not yet included)
6) Spectral Analysis (mtspec)
7) Mean Spectra and StdDev
8) Peak Mean Amplitude
9) Horizontal Geometric Mean
10) Extract Vertical Peak
11) Spectral Ratio

Coded plotting options:
1) Plot Spectra (plots the spectral traces obtained)
2) Plot Spectral Mean and StdDev (plots only the spectral mean and one standard deviation)
3) Plot Pectra, Mean, StdDev (plots all spectral traces, their mean, and one standard deviation)

Future plotting code additions may include:
1) Plotting bar chart for H/V values
2) Plotting station and event locations
3) Plotting spatial variability
4) Plotting azimuthal variability

Python packages needed:
1) numpy
2) matplotlib.pyplot
3) obspy
4) pandas
5) mtspec
It is recommended to create a new environment for these packages, as mtspec is no longer supported and may required downgraded components to install. 
