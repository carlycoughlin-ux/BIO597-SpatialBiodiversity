# BIO 597 Spatial Analysis of Biodiversity

An advanced survey of tools for modeling and analysis of spatial patterns of
biodiversity, including species distributions, biodiversity metrics, endemism, phylogenetic diversity,
and landscape connectivity, with emphasis on leveraging environmental drivers (e.g. remote sensing
and microclimate data) within predictive frameworks (e.g. SDMs and machine learning models).

### Local Preview

Install Zensical in a Python environment, then run:

```sh
zensical serve
```

Build the static site with:

```sh
zensical build --clean
```

## Publishing

GitHub Pages is configured through `.github/workflows/docs.yml`. In the repository settings on GitHub, set Pages to publish with GitHub Actions. Pushes to `main` will then build and deploy the site to:

https://isaacovercast.github.io/BIO597-SpatialBiodiversity/
