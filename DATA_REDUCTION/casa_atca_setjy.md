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
