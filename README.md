# Anatomy Curvature Analysis

## Overview
This MATLAB project calculates and visualises three types of curvature (normal, mean and Gaussian) on triangulated STL surfaces (e.g. the pelvis). Although it was developed for orthopaedic research, it can be applied to other anatomical structures. As well as pure curvature analysis, the project generates colour-coded STL models, marks areas of high curvature, and provides figures that can be used to validate defect areas (e.g. distances from defect boundaries to regions of high curvature).

## Key Features:
1. **Multiple Curvature Measures**  
   - Normal curvature: angle-based over adjacent face normals  
   - Mean curvature: based on Subburaj et al.; angle-based over adjacent face normals with edge and surface weighting  
   - Gaussian curvature: based on Subburaj et al.; angle sum around the vertex / distribution deficit  

2. **Robust for Open Meshes**: Identify the boundary vertices/faces  
3. **Neighbourhood Topology**: Adjacency of vertices and faces; edge lengths and triangle areas for weighting  
4. **Colour-Coded STL**: Percentile-based normalisation of curvature values, viridis colormap, convert colours in STL (16-bit ARGB)  
5. **Top Curvature Regions (Validation)**: Threshold value above top x% of curvature values, distances from boundary vertices to top curvature points  

## How to Use:
1. **Code Structure**: The Curvature Class can be integrated into a corresponding main script. The key parts of the code are extracted into individual functions for reuse.  
2. **Import**: Import the anatomical model data in STL format (triangulated).  
3. **Run Curvature Calculations**  
4. **Results**: The characteristic values for normal, mean and Gaussian curvatures are stored. A colour-coded STL file is output with the corresponding curvature values.  

## Use Cases:
- **Orthopaedics/Biomechanics**: Acetabulum defect characterisation, surface quality of anatomical models  
- **General Morphology**: Curvature-based landmark finding / ROI detection  

## Benefits:
- Provides multiple curvature methods and validation for surface analysis  
- Curvature methods robust with open meshes  
- Covers the full workflow: from mesh pre-processing to STL colour output  
- Efficient and comprehensive visualisation of anatomical models  
- Modular: individual functions can be used separately in other pipelines  

## Compatibility:
This class is compatible with MATLAB and can easily be integrated into existing workflows for analysing the curvature of anatomical models.  
Optimised for MATLAB 2024a but should be compatible with the most recent versions of MATLAB.  

**Toolbox required**: Statistics and Machine Learning Toolbox (for the `knnsearch` function).  

## Disclaimer:
This MATLAB class is provided on the MATLAB File Exchange for educational and research purposes. Users should ensure that the class meets their specific analysis requirements and may need to adapt it accordingly. The code is provided "as-is," and the author assumes no responsibility for its use or any consequences thereof.  

## Keywords:
biomedical modeling, curvature, mean curvature, gaussian curvature, surface analysis, stl, pelvis, mesh processing, orthopaedics, triangulation, viridis  

## References:
- M. P. Do Carmo, *Differential Geometry of Curves and Surfaces*, 2nd ed. A K Peters/CRC Press, 2010.  
- M. Meyer, M. Desbrun, P. Schröder, and A. H. Barr, “Discrete Differential-Geometry Operators for Triangulated 2-Manifolds,” *Visualization and Mathematics III*, pp. 35–57, 2003.  
- K. Moreland, “Why we use bad color maps and what you can do about it,” *Human Vision and Electronic Imaging*, 2016.  
- K. Subburaj, B. Ravi, and M. G. Agarwal, “3D shape reasoning for identifying anatomical landmarks,” Ph.D. dissertation, 2008.  
- K. Subburaj, B. Ravi, and M. Agarwal, “Automated identification of anatomical landmarks on 3D bone models reconstructed from CT scan images,” *Computerized Medical Imaging and Graphics*, vol. 33, no. 5, pp. 359–368, 2009.  
- W. Wilke, *Segmentierung und Approximation großer Punktwolken*, Dissertation, Technische Universität Darmstadt, 2002.  
- Y. Zhang, M. Fjeld, M. Fratarcangeli, A. Said, and S. Zhao, “Affective colormap design for accurate visual comprehension in industrial tomography,” *Sensors*, vol. 21, no. 14, pp. 1–20, 2021.  

## Cite As:
- Carina Micheler (2025). *Anatomy Curvature Analysis* (https://www.mathworks.com/matlabcentral/fileexchange/181273-anatomy-curvature-analysis), MATLAB Central File Exchange. Abgerufen 28. August 2025.  
