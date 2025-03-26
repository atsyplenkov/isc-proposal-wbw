# Bridging R and Whitebox Workflows

A proposal for the 2025 ISC Grant Program, based on the [RConsortium/isc-proposal](https://github.com/RConsortium/isc-proposal) template

## Technical aspects

The current project uses `renv` as an R environment manager and `quarto` for PDF rendering. Some custom fonts are expected to be installed on your system to ensure error-free PDF compilation:

- [Inter](https://fonts.google.com/specimen/Inter)
- [Fira Code](https://fonts.google.com/specimen/Fira+Code)
- [Jost](https://fonts.google.com/specimen/Jost)

To render the PDF, run `quarto render isc-proposal.qmd` from the project directory.

## Repository structure

```
├───assets
├───data
├───figures
├───proposal
├───src
└───_extensions
```

Intermediate results of several scripts are stored in the `data` folder, such as Stack Exchange responses. This is done to avoid overusing the free API.

Figures are saved using `ggsave` into the `figures` directory, with custom `.svg` files stored in an `assets` folder. The `src` directory contains custom `ggplot2` themes and functions.