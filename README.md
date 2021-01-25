# ![Flux::](include/favicon-32x32.png ':class=img-title') Flux:: Documentation

This directory contains documentation for Flux:: products
To browse it go to https://doc.flux.audio.

## Development

## Python virtual env

Create a virtual python environment :

```sh
python3.9 -m venv env
source ./env/bin/activate
```

Install the requirements :

```sh
pip install -r requirements.txt
```

## Build sphinx doc

```sh
make html # without make use : sphinx-build -b html . build
```


