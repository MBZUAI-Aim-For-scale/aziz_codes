# aziz_codes

This repository contains a collection of Jupyter notebooks and scripts used for climate, weather, and geospatial analysis.

You can run the code in **two different ways**, depending on your setup and laptop specifications.

---

## 🚀 How to Run the Code

You have **two options**:

---

## ✅ 1. Run Using DevContainers (Recommended if you have similar laptop specs)

If your machine supports Docker and has similar hardware specifications, you can run everything using the provided **DevContainer** setup.

### Steps

1. Install **Docker Desktop**  
   👉 https://www.docker.com/products/docker-desktop/

2. Install **Visual Studio Code (VS Code)**  
   👉 https://code.visualstudio.com/

3. In VS Code, install the extension:  
   - **Dev Containers** (ID: `ms-vscode-remote.remote-containers`)

4. Clone this repository and open the folder in VS Code.

5. When prompted, click:  
   **“Reopen in Container”**  
   or open the Command Palette and choose:  
   **“Dev Containers: Reopen in Container”**

6. VS Code will build the Docker environment using the `.devcontainer` configuration.  
   Once the container is up, you can run all notebooks and scripts inside that environment.

---

## ✅ 2. Run Locally on Your Laptop (Manual Installation)

If you prefer to run the code directly on your laptop without Docker, you must install all required dependencies manually.

### Requirements

Make sure you have:

- Python 3.10+  
- (Optional but recommended) CUDA support for GPU if you want to use PyTorch with GPU.

### Install Dependencies

You can install the libraries listed below (e.g. via `requirements.txt`):

```txt
--extra-index-url https://download.pytorch.org/whl/cu128
--no-binary=numcodecs

# make Beam happy
numpy==2.2.6

# keep zarr/numcodecs combo that exposes blosc cbuffer_* symbols
zarr==2.17.2
numcodecs==0.11.0

# real PyPI version that works with the above
xarray-beam==0.5.1

torch
torchvision
torchaudio

anemoi-inference[huggingface]==0.4.9
anemoi-models==0.3.1
earthkit-regrid==0.4.0
ecmwf-opendata
netcdf4
h5netcdf
gcsfs
matplotlib
cartopy
jupyterlab
ipywidgets
streamlit
panel
hvplot
geoviews
geopandas
plotly
psutil
apache-beam
git+https://github.com/google-research/weatherbench2.git@main
git+https://github.com/google-research/weatherbenchX.git@main
