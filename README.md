
<!-- README.md is generated from README.Rmd. Please edit that file -->

# filter-slides-demo

<!-- badges: start -->
<!-- badges: end -->

The goal of filter-slides-demo is to demonstrate how slides can be
conditionally excluded with help of a lua-filter.

## Render through code

To render the full slide deck (including all slides):

`quarto::quarto_render("filter-slides-demo.qmd", output_file = "advanced-output.html")`

If you want to exclude the ones with the given class `.advanced {}` you
can add the lua-filter as a pandoc argument, like this:

`quarto::quarto_render("filter-slides-demo.qmd", output_file = "basic-output.html", pandoc_args ="--lua-filter=hideadvanced.lua")`

## Render through RStudio UI-button

You can specify the lua-filter in the YAML as well with:

    ---
    filters: 
      - hideanswers.lua
    ---
