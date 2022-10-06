### Hi there 👋, I'm Alex!

<!--
**s3alfisc/s3alfisc** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:

- 🔭 I’m currently working on ...
- 🌱 I’m currently learning ...
- 👯 I’m looking to collaborate on ...
- 🤔 I’m looking for help with ...
- 💬 Ask me about ...
- 📫 How to reach me: ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...
-->

In my free time, I develop R packages that implement various inference procedures for linear regression:

+ Clustered Errors 

  + [`fwildclusterboot`](https://github.com/s3alfisc/fwildclusterboot) implements the fast **wild cluster bootstrap** algorithm as suggested in [Roodman, MacKinnon, Nielsen & Webb](https://journals.sagepub.com/doi/abs/10.1177/1536867X19830877) for a range of regression packages in R. It also ports functionality from [WildBootTests.jl](https://github.com/droodman/WildBootTests.jl) to R, e.g. the WRE bootstrap for instrumental variables. 
  *News*: the development version contains implementations of new wild cluster bootstrap variants following [MacKinnon, Nielsen & Webb (2022)](https://www.econ.queensu.ca/sites/econ.queensu.ca/files/wpaper/qed_wp_1485.pdf) and support for the [Sun-Abraham Event Studies Estimator](https://www.sciencedirect.com/science/article/abs/pii/S030440762030378X) via `fixest::sunab()`.
  
  + [`summclust`](https://github.com/s3alfisc/summclust) and [`CRV3J`](https://github.com/s3alfisc/CRV3J) implement the **Jackknive CRV3 estimator** for clustered covariances as suggested by [MacKinnon, Nielsen & Webb (2022)](https://arxiv.org/abs/2205.03288). `summclust` further computes a range of leverage measures for cluster robust inferences (as in the [`summclust`](https://github.com/mattdwebb/summclust) Stata package).

+ Resampling Based Multiple Testing Corrections

  + [`wildrwolf`](https://github.com/s3alfisc/wildrwolf) implements the multiple-hypothesis correction by Romano & Wolf (2005) - as implemented in the [`rwolf`](https://docs.iza.org/dp12845.pdf) Stata package - for regression objects from the `fixest` package. 

  + [`wildwyoung`](https://github.com/s3alfisc/wildwyoung) implements the multiple-hypothesis correction by Westfall & Young (1993) - as implemented in the [`wyoung`](https://github.com/reifjulian/wyoung) Stata package - for regression objects from the `fixest` package. 

  Because both `wildrwolf` and `wildwyoung` are build around `fwildclusterboot` and the wild (cluster) bootstrap, both packages are usually quite fast.
  
