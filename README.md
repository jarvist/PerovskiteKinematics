# Perovskite Kinematics

A reprint of the Poster (PDF) is available here.

[Poster Reprint >](https://github.com/jarvist/PerovskiteKinematics)

# Ab-initio Molecular Dynamics

A single Metyl-Ammonium at the centre of a 2x2x2 supercell expansion is represented.

```
2x2x2 Supercell; based on an expansion of a relaxed Pseudo-cubic
PBESol functional (corrected GGA)
Gamma point calculation
0.5 fs integration timestep for molecular dynamics
58 ps / 2319 frames total simulation time (this analysis)
~120 hours of computation on 96 cores on EPSRC ARCHER
```

<a href="http://www.youtube.com/watch?feature=player_embedded&v=Rr2DDiYUoNA" target="_blank"><img src="http://img.youtube.com/vi/Rr2DDiYUoNA/0.jpg" 
alt="Single MA molecule from 2x2x2 Molecular Dynamics" width="480" height="360" border="10" /></a>

# Starrynight - on lattice dipole simulation

Custom C codes evaluating classical Hamiltonian on a cubic lattice. Due to the simplicity of the Hamiltonian, many million moves can be attempted per second. This allows for a study of relatively long time frames, with fairly equilibrated statistics, on device-sized segments of the Perovskite material.

The code is now fully 3D; data presented in the paper is 2D as this is easier to understand visually.

So far the parameters are calculatd for the methyl-ammonium ions rotating themselves, but equivalent physics would be produced by the inorganic cage distorting and losing centrosymmetry itself.

# Landau Phase Behaviour

By introducing an additional, local, strain term into our Hamiltonian (parameterised from a 4x4x4 supecell periodic DFT calculation of aligned MA domains, where we flip a single MA ion), we can induce the formation of fully ferroelectric domains. 

The degree of overall alignment of the simulation volume can be easily tracked by defining a Landau order parameter, the most simple of which is simply the vector average of the MA alignments. For a fully aligned domain, the length of this vector is 1, otherwise ~0.

<a href="http://www.youtube.com/watch?feature=player_embedded&v=xppLrcvCjW8" target="_blank"><img src="http://img.youtube.com/vi/xppLrcvCjW8/0.jpg" 
alt="StarryNight - 2D with CageStrain; 80x80 formation of ferroelectric domains ; Geometric Time " width="480" height="360" border="10" /></a>

The above video shows the MA domains on the left, with the resulting dipole electrostatic potential on the right. The time (or more formally, the number of Monte-Carlo moves attempted per frame) accelerates geometrically, as the ripening process of the domains becomes progressively slower.

# More Information

[MAPI MD video download (Figshare)](http://figshare.com/articles/Methyl_Ammonium_Lead_Iodide_MAPI_Pervoskite_2x2x2_Supercell_MD/1061490)

## Our Codes

[StarryNight >](https://github.com/WMD-Bath/StarryNight)

[MAPI-MD-analysis >](https://github.com/jarvist/MAPI-MD-analysis)

## Our Papers

**Molecular ferroelectric contributions to anomalous hysteresis in hybrid perovskite solar cells ￼**
APL Mat. 2, 081506 (2014); http://dx.doi.org/10.1063/1.4890246

**Atomistic Origins of High-Performance in Hybrid Halide Perovskite Solar Cells**
Nano Lett., 2014, 14 (5), pp 2584–2590 http://dx.doi.org/10.1021/nl500390f
