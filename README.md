# Kinetic modeling of acedogenic fermentation in a batch reactor

**Introduction** -
Acidogenic fermentation is a technology that is used to produce hydrogen and volatile fatty acids in an environmental friendly way. In an acidogenic fermentation carried out by a mixed culture,the microorganisms produce a spectrum of metabolic products. Consequently, the hydrogen yields achieved are lower than the maximum theoretical hydrogen yield (4 mol H2/mol glucose) when acetic acid is the end-product. However, mixed culture also has some advantages because no sterilization is required. Major assumption associated with this study is that the culture is well mixed. 

**Research article** -
"Kinetic model and study of the influence of pH, temperature and undissociated acids on acidogenic fermentation" was chosen for the course project.
Citation - Infantes, D., del Campo, A. G., Villaseñor, J., & Fernández, F. J. (2012). Kinetic model and study of the influence of pH, temperature and undissociated acids on acidogenic fermentation. Biochemical engineering journal, 66, 66-72.

**Kinetic model and parameters** -
The following equations and info is used to describe the monod-type kinetics of acidogenic fermentation:

Let:-
- x(t) is the concentration of biomass in the reactor $gSSV/l$
- s(t) is the substrate concentration $mM$ and $s_0$ be the concentration of substrate in the feed line, is equal to 50 mM
- mu is the specific growth rate parameter $h^{-1}$.
- ks is the substrate half saturation constant $mM$.
- b is the decay coefficient $h^{-1}$
- kbio is the undissociated acids threshold concentration $mM$ which caused an important shift on biomass growth 
- ksub is the undissociated acids threshold concentration $mM$ which caused an important shift on substrate fermentation
- CHA is the total concentration of undossociated acids $mM$
- Yobs is the observed biomass yield $gssv/mM of glucose$ and is calcualted using $Yobs = Yxmax(1-m)$
- m is fraction of substrate consumed for maintenance

\begin{align}

\dot{x} = \mu \frac{s(t)}{ks+s(t)} \frac{1}{1+1.2^{(CHA - kbio)}} x(t) - b x(t)\

\dot{s} = \frac{-1}{Yobs} \frac{s(t)}{ks+s(t)} \frac{1}{1+1.2^{(CHA - ksub)}} x(t)

\end{align}

However, there are several **unknown parameters that we need to estimate**:

- mu is the specific growth rate parameter $h^{-1}$
- ks is the substrate half saturation constant $mM$.
- b is the decay coefficient $h^{-1}$
- kbio is the undissociated acids threshold concentration $mM$ which caused an important shift on biomass growth 
- ksub is the undissociated acids threshold concentration $mM$ which caused an important shift on substrate fermentation
- m is fraction of substrate consumed for maintenance

**Methodology** -
Experiments were performed and model results were validated in the publication. In this study, experimental data was extracted from the article and fit into the ODE model. Next, parametric sensitivity was performed globally and locally to determine which parameter is more senitive compared to the others. Finally, bifurcation analysis was performed for the chosen variable and parameter.

**The following figures represent the experimental data** -

![download (8)](https://github.com/LAA147/Project2/blob/main/download%20(8).png)

![download (9)](https://github.com/LAA147/Project2/blob/main/download%20(9).png)

**The following figures represent fitting the experimental data with the model data** -

![download (10)](https://github.com/LAA147/Project2/blob/main/download%20(10).png)

![download (11)](https://github.com/LAA147/Project2/blob/main/download%20(11).png)

**Parametric sensitivity analysis** - 
Both global & local sensitivity analysis was performed on the model to check which parameter is more sensitive and can disturb the model when changed. Each parameter was varied by 20% for the global analysis. Where as, for the local analysis, each parameter was varied by 1%.

Global sensitivity results- 

![download (12)](https://github.com/LAA147/Project2/blob/main/download%20(12).png)

Local sensitivity results- 

![download (13)](https://github.com/LAA147/Project2/blob/main/download%20(13).png)

From the statistical analysis, it can be predicted that 'b' parameter (represents decay coefficient) is the most sensitive parameter. This paramter is further used to perform the bifurcation analysis.

**Bifurcation analysis** -
Bifurcation analysis was performed on the substrate concentration variable to plot ds/dt vs s by varying the most sensitive parameter "b". The results are as follows:

![download (14)](https://github.com/LAA147/Project2/blob/main/download%20(14).png)

**Conclusions** - 
Both my null hypothesis should be rejected because of the obtained p-value. From the linear regression analysis, a positive dependence of births data is observed, a negative dependence of income data is observed and a positive dependence of their interaction is noted.


**Next steps** - 
For a better analysis/fit, a non-linear model can be used. Also, more data points can be incorporated to analyze the above mentioned parameters. For example, data from 2021, 2022 years can be collected and analyzed accordingly.
