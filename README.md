# Kinetic modeling of acedogenic fermentation in a batch reactor

**Introduction** -
Acidogenic fermentation is a technology that is used to produce hydrogen and volatile fatty acids in an environmental friendly way. In an acidogenic fermentation carried out by a mixed culture,the microorganisms produce a spectrum of metabolic products. Consequently, the hydrogen yields achieved are lower than the maximum theoretical hydrogen yield (4 mol H2/mol glucose) when acetic acid is the end-product. However, mixed culture also has some advantages because no sterilization is required. Major assumption associated with this study is that the culture is well mixed. 

**Research article** -
"Kinetic model and study of the influence of pH, temperature and undissociated acids on acidogenic fermentation" was chosen for the course project.
Citation - Infantes, D., del Campo, A. G., Villaseñor, J., & Fernández, F. J. (2012). Kinetic model and study of the influence of pH, temperature and undissociated acids on acidogenic fermentation. Biochemical engineering journal, 66, 66-72.

**Kinetic model and parameters** -
The following equations and info is used to describe the monod-type kinetics of acidogenic fermentation:

Let:-
- x(t) is the concentration of biomass in the reactor ($gSSV/l$). 
- s(t) is the substrate concentration ($mM$) and $s_0$ be the concentration of substrate in the feed line, is equal to 50 mM.
- mu is the specific growth rate parameter $h^{-1}$.
- ks is the substrate half saturation constant $mM$.
- b is the decay coefficient ($h^{-1}$)
- kbio is the undissociated acids threshold concentration ($mM$) which caused an important shift on biomass growth 
- ksub is the undissociated acids threshold concentration ($mM$) which caused an important shift on substrate fermentation
- CHA is the total concentration of undossociated acids ($mM$)
- Yobs is the observed biomass yield ($gssv/mM of glucose$) and is calcualted using $Yobs = Yxmax(1-m)$
- m is fraction of substrate consumed for maintenance

\begin{align}
\dot{x} = \mu \frac{s(t)}{ks+s(t)} \frac{1}{1+1.2^{(CHA - kbio)}} x(t) - b x(t)\\
\dot{s} = \frac{-1}{Yobs} \frac{s(t)}{ks+s(t)} \frac{1}{1+1.2^{(CHA - ksub)}} x(t)
\end{align}

However, there are several **unknown parameters that we need to estimate**:

- mu is the specific growth rate parameter $h^{-1}$
- ks is the substrate half saturation constant $mM$.
- b is the decay coefficient ($h^{-1}$)
- kbio is the undissociated acids threshold concentration ($mM$) which caused an important shift on biomass growth 
- ksub is the undissociated acids threshold concentration ($mM$) which caused an important shift on substrate fermentation
- m is fraction of substrate consumed for maintenance

**Methodology** -
Experiments were performed and model results were validated in the publication. In this study, experimental data was extracted from the article and fit into the ODE model. Next, parametric sensitivity was performed globally and locally to determine which parameter is more senitive compared to the others. Finally, bifurcation analysis was performed for the chosen variable and parameter.

**The following figures represent the experimental data** -


