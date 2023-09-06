# Protein_pockets

# Data Folder

The data folder contains all of the protein pockets data used in the analysis of both the 3D voxellization and DScore statistical Analysis

# 3D Voxelization

3D space voxellization can be used for utilizing datadriven approaches that rely solely on structural information to visualize ligands as spatial fields within target protein pockets. Proteins exhibit a diverse range of shapes, yet nature often utilizes recurring patterns at various levels. Identifying and categorizing these similarities is crucial for comprehending evolutionary processes. The data used for space voxellization was taken from fpocket. The steps to complete this algorithm were as follows: 

  ## 1. Filter the pockets to retain only those with a druggability score greater than 0.5. 
  ## 2. Assume a single pqr file as input, containing the alpha spheres that define the pocket. 
  ## 3. Calculate the bounding box (min, max, xyz) of the alpha spheres, counting their centers and radii. Name these bounding box coordinates as xmin and xmax ∈ R3. 
  ## 4. Add a margin L to each side of the bounding box. 
  ## 5. Determine the center of the bounding box and designate it as x0 ∈ R3. 
  ## 6. Compute the coordinates of an imaginary 3D grid centered on x0. The grid spacing must be dX (as- sumed to be 1  ̊A). Ensure the grid covers the entire bounding box + L, rounding up as necessary to maintain a square grid. 
  ## 7. Assign coordinates xi and values vi to each cell of the grid. For each cell, set vi to 1 if xi is inside any alpha-sphere, otherwise set it to 0. 8. Return the grid, including its coordinates, bounding box, and values. 
  
  Further use of this voxellized representations of protein pockets enable efficient ligand binding prediction, virtual screening for drug discovery, structural analysis, and protein design and engineering by capturing the spatial distribution of pocket features for analysis, prediction, and modification.

  # Feature Selection Classification

  ## Simplification of protein pocket DScore evaluation

  Druggability score classification using random forrest and K-mean clustering was then conducted on the most relevant set of features
  
  ## 1. We characterize and reduce the number of features that are most important to classify and define the druggability scores of protein pockets into two classes
  ## 2. To select and filter out the most important features that play an important role in the DScore prediction of protein pockets
