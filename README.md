# RxNav IN A BOX

## Pre-Requisutes

Launch RxNav-in-a-Box Docker container on local computer.
OR use RxNav Public API address.

A web version for public use, as well as overview guides, technical documentation, and news, can be found at [Web Version](https://rxnav.nlm.nih.gov/).

## Docker Container

Navigate to:

[local instance](http://localhost:4000/)

[RxNav](http://localhost:4000/RxNav/)

The API resources can also be used interactively or in batch mode with RxMix: [RxMix](http://localhost:4000/RxMix/)

[RxClass](http://localhost:4000/RxClass/)

[RxNorm API Docs](http://localhost:4000/RxNormAPIs.html)

[Prescribable RxNorm API Docs](http://localhost:4000/PrescribableAPIs.html)

[RxTerms API](http://localhost:4000/RxTermsAPIs.html)

[RxClass API](http://localhost:4000/RxClassAPIs.html)

## Install Deps and Launch

`pip install notebook jupyterlab ipykernel`

Register environment as a Jupyter Kernal: `python -m ipykernel install --user --name myenv --display-name "Python (myenv)"`

    - Internal name: --name myenv
    - "Python (myenv)" is the kernel list name

Open in browser: `jupyter lab`
