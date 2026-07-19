# Cardiac-Modeling_Fiber-Field-Generation-Project
This repository contains the implementation of the Laplace-Dirichlet-Rule-Based Method (LDRBM) for cardiac fiber field generation in a left ventricle geometry and electrophysiology simulation of the activation maps of the isotropic and anisotropic case. 
The project is based on the framework proposed by _Piersanti et al. (2021)_.

The workflow of the project follows an incremental approach to validate the fiber generation algorithm.

## Project Overview
The workflow follows an incremental approach to validate the fiber generation algorithm and the electrophysiological solver:
1. **Cube Geometry**: Initial validation of the LDRBM algorithm on a simple cubic domain.
2. **Idealized Ventricle**: Implementation of fiber generation on a simplified ventricular geometry to test curvature handling.
3. **Realistic Ventricle**: Application of the LDRBM method to a high-resolution anatomical left ventricle mesh.
4. **Electrophysiological Simulation**: Solving the monodomain equation to generate activation maps, comparing isotropic vs. anisotropic conductivity tensors.

## Prerequisites
- Firedrake 
- NumPy
- PyVista (for 3D visualization)

## How To Run
The project's code is organized in a modular sctructure to facilitate the use, it was originally implemented in Colab. 
In order to use it:
1. Ensure the mesh files '_lv_epi_0.stl_' and '_lv_epi_0.stl_' are in the directory (necessary for the realistic left ventricle mesh)
2. Run the script, obtain the images, interactive plots, GIFs, videos and output '.vtu' files that can be visualized using ParaView.

3. ## Results
Visualizations of the fiber fields and activation maps are available in the `results/` folder.

## Acknowledgments
The ventricular mesh used in this study was sourced from [https://zenodo.org/] and processed for Firedrake compatibility.
