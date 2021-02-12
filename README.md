# Sagitta_Checks

## Initial conclusions: ##

- pre-main sequence probability varies as expected for empirical
populations (but 95% appears a more secure threshold than 80%, based
on open cluster tests):
    - flags large fraction of Upper Sco YSOs; (see
      [pms prob. histograms for upper sco members at actual distances](https://github.com/kevincovey/Sagitta_Checks/blob/main/plots/compareUpperScoProbs.png))
    - flags a smaller, age-dependent fraction of open cluster members;
      (see
      [pms prob. histograms for open cluster members at actual distances](https://github.com/kevincovey/Sagitta_Checks/blob/main/plots/CoronaeProbs.png),
      and stats computed in cell 5 of [open cluster notebook](https://github.com/kevincovey/Sagitta_Checks/blob/main/notebooks/ShiftOlderClusters.ipynb))
	- flags a very small (but non-zero) fraction of field stars (see
      [pms prob histograms of field stars at actual distances](https://github.com/kevincovey/Sagitta_Checks/blob/main/plots/DANCeProbs.png))

- properties of known YSOs, at their actual distances, are in the
right ballpark:
    - [Extinctions are reasonable](https://github.com/kevincovey/Sagitta_Checks/blob/main/plots/compareAv.png), though fairly uniform + underestimated in the mean (sinceonly considering foreground component) 


### Sagitta Inputs+outputs for catalogs with distance shifted copies: ###

- Catalog of likely members of young (ages 30-300 Myr) open clusters
    (from
[Meingast, Alves & Rottensteiner 2021](https://ui.adsabs.harvard.edu/abs/2021A%26A...645A..84M/abstract),
via
[Vizier](https://vizier.u-strasbg.fr/viz-bin/VizieR?-source=J/A+A/645/A84)
and TOPCAT to match to Gaia + 2MASS)

    Distance Filtering: catalog synthetically shifted to distances between
10-500pc, in steps of 30 pc (original locations also retained,
including many > 500pc)

    [Sagitta Inputs](https://www.dropbox.com/s/wqcbdxr44femxl2/LongerCoronae.fits?dl=0)
| [Sagitta Outputs](https://www.dropbox.com/s/v7xcbreyrsk865g/LongerCoronae-sagitta.fits?dl=0)

- Catalog of field stars in direction of IC 4665
    (Pmem < 0.3 sources from
[Miret-Roig+ 2019](https://ui.adsabs.harvard.edu/abs/2019A%26A...631A..57M/abstract),
via
[Vizier](https://vizier.u-strasbg.fr/viz-bin/VizieR-3?-source=J/A%2bA/631/A57/table5)
)

     Distance Filtering: catalog synthetically shifted to distances between
10-500pc, in steps of 30 pc (original locations also retained,
including many > 500pc)

    [Sagitta Inputs](https://www.dropbox.com/s/nnwn10160o7js2r/LongerDANCe.fits?dl=0) | [Sagitta Outputs](https://www.dropbox.com/s/e93kfdoow7i2702/LongerDANCe_results.fits?dl=0/)

