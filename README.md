# HES-S-Matrix
Contains mathematica notebooks to compute S-Matrix of highly excited physical string states (HES) and tachyons (T). This is based on the article [arXiv:2312.02127](https://arxiv.org/abs/2312.02127).

This repository contains 3 notebooks:

## 1. HHT_amplitude_particular_partitions.nb
Computes the HES-HES-T scattering for two particular partitions of $N_1$ and $N_2$ respectively. The scattering amplitude is expressed both analytically as an expression of kinematic variable $\chi$ and numerically as data points at $\chi_i$ grid points. The kinematic choices are as described in the aforementioned article.
> [!CAUTION]
> For $\zeta_1 \cdot \zeta_2 \neq 0$, evaluation can take considerable time for $`N_1, ~ N_2 > 10`$; especially for the partitions with low mode numbers (i.e, $` \{ 1,1,1,\cdots \}, ~ \{2,1,1,\cdots \} `$ etc).


## 2. HHT_amplitude_all_partitions.nb
Computes the HES-HES-T scattering for all the partitions of $N_1$ and $N_2$. This notebook stores the peak positions in $\chi$, the corresponding peak amplitudes, and the level spacings between the peak positions in 3 separate files. To import these data files in Mathematica, follow the instructions mentioned in the notebook. The kinematic choices are again as described in the aforementioned article.
> [!CAUTION]
> For $`\zeta_1 \cdot \zeta_2 \neq 0`$, evaluation can take considerable time for $`N_1, ~ N_2 > 10`$.


## 3. ETH_fomega_computation.nb
Computes coarse-grained $` \langle HES (N_1) | T | HES (N_2) \rangle `$ for $`N_1 \neq N_2`$ (i.e, off-diagonal S_Matrix elements) with normalized $`| HES \rangle`$ states and calculates $`f (\omega)`$ from the elements. This is done only for the $` \zeta_1 \cdot \zeta_2 = 0 `$ case. This notebook stores both the matrix elements and $`f(\omega)`$ in two separate files. The latter one is saved in the format $` \{ \cdots , \{\omega_i, f(\omega_i) \}, \cdots \} `$ with $` \omega_i `$ being the grid points.

For more details, look into the article.

> [!TIP]
> It is better to set directories in all three notebooks to keep track of the files stored. Uncomment the notebook cells containing `SetDirectory` command to set your desired directories. 
