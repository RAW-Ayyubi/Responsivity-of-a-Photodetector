# Responsivity-of-a-Photodetector
Making predictions for the responsivity of a photodetector based on various input features, including the active layer, substrate, and experimental conditions.

About the input file "InputData.csv":
This file contains 1,400 sample points for training, primarily derived from 20 experimental studies. Additional properties of these materials have been collected from various theoretical studies, the Materials Project, and the NIST database.

To run the code
Download the input file "InputData.csv" and update the file path in the code "Responsivity_Predictions.ipynb" to match the location of the input file on your computer. Then, run the code to train various regression models and make predictions for the responsivity of a device. This device is composed of an active layer and a substrate under various experimental conditions, as described below:

Active Layer Features:
Total atomic number
Average atomic number
Average valence electrons
Density
Mobility
Attenuation coefficient
Experimental band gap
Theoretical band gap
Thickness

Substrate Features:
Experimental band gap

Experimental Conditions:
Bias voltage
Wavelength of incident photons
Power intensity of incident photons

Target Variable:
Responsivity
