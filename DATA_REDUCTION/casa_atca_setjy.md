### 利用ATCA calibrator database计算casa中setjy的参数

**Useful links**:
> Description for `setjy` task: https://casa.nrao.edu/casadocs/casa-5-1.2/global-task-list/task_setjy/about \
> Description for coefficients in the atca calibrator database: https://www.narrabri.atnf.csiro.au/calibrators/calibrator_database_documentation.html#interpreting-spectral-indices

在casa中，setjy的变量`spix`可以包含高阶量，model满足

$$
S(\nu) = S(\nu_0) \left(\cfrac{\nu}{\nu_0}\right)^{\alpha_0 + \alpha_1\log(\nu/\nu_0) + ...}
$$

而在atca calibrator database中，model的计算为

$$
\log S(\nu) = c_0 + c_1\log\nu + c_2(\log\nu)^2 + ...
$$

如果取$\nu_0 = 1$ (GHz), 那么casa中的公式变成

$$
\log S(\nu) = \log S(\nu_0) + \alpha_0\log\nu + \alpha_1(\log\nu)^2 + ...
$$

因此在设置setjy时，取`reffreq`为'1000.0MHz'，`fluxdensity[0]`为$10^{c_0}$，而`spix`取[$c_1$, $c_2$]
