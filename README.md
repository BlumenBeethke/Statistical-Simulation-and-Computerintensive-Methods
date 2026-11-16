# Statistical Simulation and Computer-Intensive Methods

This repository contains four R Markdown exercises on numerical stability and statistical computing:

1. [Exercise 1: Variance after a change of origin](./1.AssExercise1.Rmd) compares variance algorithms and demonstrates cancellation error when data have a large offset.
2. [Exercise 2: A probability that disappears](./1.AssExercise2.Rmd) compares normal upper-tail calculations and shows why direct tail probabilities are more reliable than subtracting from one.
3. [Exercise 3: Comparing two models without computing their likelihoods](./1.AssExercise3.Rmd) demonstrates likelihood underflow and compares direct likelihoods with log-likelihoods.
4. [Exercise 4: Diagnosing a numerically suspicious covariance matrix](./1.AssExeercise4.Rmd) examines covariance calculations for highly correlated variables with a large offset, including the effect of centering.

Each document includes a fixed random seed where it generates random data, making those results reproducible.

## Rendering PDFs

Install R, the `rmarkdown` package, and [Tectonic](https://tectonic-typesetting.github.io/). From the repository directory, run:

```sh
Rscript -e 'for (input in Sys.glob("*.Rmd")) { output <- paste0(tools::file_path_sans_ext(input), ".pdf"); rmarkdown::render(input, output_format = rmarkdown::pdf_document(latex_engine = "tectonic"), output_file = basename(output)) }'
```

This creates a PDF alongside each R Markdown source file, using the same base filename. The documents also declare GitHub Markdown output, which can be rendered individually with:

```sh
Rscript -e 'for (input in Sys.glob("*.Rmd")) rmarkdown::render(input, output_format = "github_document")'
```
