# Statistical Simulation and Computer-Intensive Methods

## Exercise 1: Variance after a change of origin

[1.AssExercise1.Rmd](./1.AssExercise1.Rmd) explores how adding a constant affects numerical calculations of sample variance. It compares R's `var()` with two-pass and one-pass variance algorithms across several offsets, then discusses cancellation error and centering data before computing descriptive statistics.

The document uses a fixed random seed so its generated sample and results are reproducible.

## Rendering

Install R and the `rmarkdown` package. To render the GitHub Markdown output:

```sh
Rscript -e 'rmarkdown::render("1.AssExercise1.Rmd", output_format = "github_document")'
```

To render a PDF, also install [Tectonic](https://tectonic-typesetting.github.io/) and run:

```sh
Rscript -e 'rmarkdown::render("1.AssExercise1.Rmd", output_format = rmarkdown::pdf_document(latex_engine = "tectonic"))'
```

The rendered files are written alongside the source document.
