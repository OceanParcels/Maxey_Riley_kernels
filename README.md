# Maxey_Riley_kernels
Advection kernels to advect particles using the full maxey-riley (MR) equations and the slow manifold (SM) MR equations. 
This project contains the folder `functions` and `benchmarks`. We still need to include correct handling of the boundaries
of the flowfield when caluclating the derivatives.

## functions
The `kernels.py` contains the advection kernels that can be used in parcels to advect particles using the full MR equation or SM MR equation in 2D or 3D. 
We use runge-kutta 4 (RK4) as numerical integration scheme in these kernels. In addition the file contains the particle type inertial particle, 
which takes the buoyancy and stokes relaxation time used in the MR equation and the velocity of the particle (only needed for the full MR equation). 
For the full MR equations the particles need to be initialized using the InitializeParticles function aslo provided in this notebook.

## benchmarks
The benchmark folder contains 2 benchmarks. The benchmark of particles in the 2D kaufman vortex flow can be found in `Kaufmann_vortex_flow_2D.ipynb`. 
The benchmark of the 3D advection can be found in the notebook `3D_vortex_flow.ipynb`
