# Responsivity-of-a-Photodetector
Making predictions for the responsivity of a photodetector based on various input features, including the active layer, substrate, and experimental conditions.

About the input file "InputData.csv":
This file contains 1927 sample points for training, primarily derived from 29 experimental studies. Additional properties of these materials have been collected from various theoretical studies, the Materials Project, and the NIST database.

To run the code
Download the input file "InputData.csv" and update the input file path in the code "Responsivity_Prediction.ipynb" to match the location of the input data file on your computer. Then, run the code to train various regression models and make predictions for the responsivity of a device. The device is composed of an active layer and a substrate under various experimental conditions, as described below:

Active Layer Features:
Total atomic number
Average atomic number
Average valence electrons
Density
Mobility
Experimental band gap
Theoretical band gap
Thickness

Substrate Features:
Experimental band gap

Experimental Conditions:
Bias voltage
Wavelength of incident photons
Power intensity of incident photons

Seven Device Configurations: Choose one device configuration from PIN, NIP, PN, NN, FET, Ohmic, and Schottky Barrier Diode (SBD).

Target Variable:
Responsivity (A/W)

# Computational Resources Used
All computations in this study were performed on a local machine running Windows 11 Pro, equipped with an Intel Core i5-1135G7 processor (4 cores, 8 threads, 2.40 GHz) and 8 GB of RAM. The code was executed using Jupyter Notebook 6.5.7 within the Anaconda Navigator 2.6.3 environment. No GPU acceleration was used during training or inference. The complete notebook, which includes dataset assembly, model training, evaluation, and plotting, takes approximately 10 minutes to execute end-to-end on this configuration.
