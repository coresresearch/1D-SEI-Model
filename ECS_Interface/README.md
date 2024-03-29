# 1D-SEI-Model

## D. Korff and S.C. DeCaluwe
### Colorado School of Mines

This model simulates the growth of the SEI (*S*olid *E*lectrolyte *I*nterphase)
on a non-intercalating anode (in this case, tungsten).

*Note: This is a 'frozen' version of the code, used to generate the figures in the ECS 
Interface article from the Spring 2019 Data Science issue. Please note that this 
implementation is for demonstration purposes only - there are additional features yet
to be implemented, and the thermodynamics and reaction rates presented in the cti file
are not based on anything in particular (i.e. they are neither based on previous literature
nor fit to any data.*

The model is built upon the capabilities in the [Cantera](cantera.org) software
suite, which facilitates incorporating chemical complexity in an efficient,
theoretically-robust manner.

The model incorporates the following phenomena:

- Charge transfer reactions at the tungsten-SEI and SEI-electrolyte interfaces.
- Chemical reactions between SEI species and between SEI and electrolyte species.
- Capacitive double layer charging at the tungsten-SEI and SEI-electrolyte
interfaces.

The model is written in python, and makes use of several python modules, which
you will need to download before running the model.  See the header for the file
`sei_1d_model.py` for a list of these modules.  We highly recommend using
[Conda](conda.io) to manage the various dependencies.

To run the model, simply::
1. Download the files in this directory,
2. Install the necessary dependencies,
3. Open `sei_1d_inputs.py` and alter the input parameters as desired, and
4. Run from a command line via the command:

```
python model/sei_1d_model.py
```

You can also run the same file from any number of python-baseed IDEs.

For advanced operation, you can edit the thermo-chemistry in the cantera input
(CTI) file (which is currently `W_anode_chem_01072019.cti`).  It is recommended
to copy and save the file under a new name before editing, rather than directly
overwriting the present file.
