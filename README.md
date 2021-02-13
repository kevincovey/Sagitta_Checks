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

- properties of known YSOs and open cluster stars, at their actual distances, are in the
right ballpark:
    - [Extinctions are reasonable](https://github.com/kevincovey/Sagitta_Checks/blob/main/plots/compareAv.png), though fairly uniform + underestimated in the mean (since only considering foreground component)
    - [YSOs are assigned young ages (log Age = 6.5)](https://github.com/kevincovey/Sagitta_Checks/blob/main/plots/compareUpperScoAges.png), though maybe a bit low (log Age = 6.5 implies ~3 Myrs, whereas typical ages for Upper Sco range from 4-10 Myrs)
    - [Open cluster stars are assigned older ages](https://github.com/kevincovey/Sagitta_Checks/blob/main/plots/CoronaeAges.png),
and the lower confidence pms candidates are older (indicating that pms probability is a good proxy for height above the mainsequence). 
    - [field star contaminants end up with not-as-old ages, however](https://github.com/kevincovey/Sagitta_Checks/blob/main/plots/DANCeAges.png)

- distance shifted catalogs indicate that model distance has noticable impact on inferred ages; impact on pms status is smaller, but does appear to avoid assigning pms status within 100pc.
   - [dist vs. pms](https://github.com/kevincovey/Sagitta_Checks/blob/main/plots/LongerUpperScoDistPMS.png) and [dist vs. age](https://github.com/kevincovey/Sagitta_Checks/blob/main/plots/LongerUpperScoDistAge.png) for shifted Upper Sco sample
   - [dist vs. pms](https://github.com/kevincovey/Sagitta_Checks/blob/main/plots/CoronaeDistPMS.png) and [dist vs. age](https://github.com/kevincovey/Sagitta_Checks/blob/main/plots/CoronaeDistAge.png) for shifted open cluster sample
   - [dist vs. pms](https://github.com/kevincovey/Sagitta_Checks/blob/main/plots/ShiftedDANCeDistPMS.png) and [dist vs. age](https://github.com/kevincovey/Sagitta_Checks/blob/main/plots/ShiftedDANCeDistAge.png) for shifted field star sample
       - [ratio of distribution of pms probabilities](https://github.com/kevincovey/Sagitta_Checks/blob/main/plots/ShiftedDANCePMSHistRatio.png) confirms that stars are less likely to be assigned high pms probabilities if shifted within 100pc (relative to other distances within 500pc). 
       - distance effects can also be seen in raw field star sample,
         since it naturally includes more distance variation than
         Upper Sco or open cluster catalogs (see [age](https://github.com/kevincovey/Sagitta_Checks/blob/main/plots/rawDANCeDistAge.png) and
         [pms probability](https://github.com/kevincovey/Sagitta_Checks/blob/main/plots/rawDANCeDistPMS.png) vs. distance plots for the raw catalog)

- Systematic errors in age appear ~3x larger than variation implied by
scattering test ($\sigma$ ~0.3 dex vs. 0.1 dex from scattering test)
    - distribution of age offsets for synthetically shifted
      [YSOs](https://github.com/kevincovey/Sagitta_Checks/blob/main/plots/compareUpperScoAgeDiffs.png)
      and [field stars](https://github.com/kevincovey/Sagitta_Checks/blob/main/plots/ShiftedDANCeAgeDiffs.png)
    - see also stats calculated at bottom of [Upper Sco](https://github.com/kevincovey/Sagitta_Checks/blob/main/notebooks/ShiftUpperSco.ipynb) and [Field Star](https://github.com/kevincovey/Sagitta_Checks/blob/main/notebooks/ShiftFieldStars.ipynb) notebooks


### Sagitta Inputs+outputs for catalogs with distance shifted copies: ###

- Catalog of likely members of young (ages 30-300 Myr) open clusters
    (from
[Meingast, Alves & Rottensteiner 2021](https://ui.adsabs.harvard.edu/abs/2021A%26A...645A..84M/abstract),
via
[Vizier](https://vizier.u-strasbg.fr/viz-bin/VizieR?-source=J/A+A/645/A84)
and TOPCAT to match to Gaia + 2MASS)

    Distance Filtering: catalog synthetically shifted to distances between
10-500pc, in steps of 3 pc (original locations also retained,
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

