# Nursery Manual - Jupyter Book

This repository contains the source files for the **Nursery Manual** Jupyter Book, which is hosted online via GitHub Pages. The manual documents propagation, growing, and inventory management at the UBC Botanical Garden nursery.

## View the Book

You can view the Jupyter Book online here: [[UBCBG Nursery Manual](https://kkubeck.github.io/nursery-manual/)]

## Project Structure

The repository is organized as follows:

```
nursery-manual/
├── .gitignore
├── _config.yml
├── _toc.yml
├── README.md
├── index.md
├── references.bib
├── requirements.txt
├── data
│   ├── 2017-2023_all-prop.csv
│   ├── ubc_temperature91_02cl.csv
├── docs
│   ├── data_entry.md
│   ├── historical_nursery.md
│   ├── potting_media_recipes.md
│   ├── seed-sowing.md
│   ├── seed_dormancy_and_treatments.md
│   ├── test_image.md
│   ├── transplanting.md
├── images
│   ├── logo.png
│   ├── historical_nursery
│   │   ├── 2004-03-21.PNG
│   ├── test.JPG
├── notebooks
    ├── project_cold_with_graphics.ipynb
    ├── seed_pot_RQ_count.ipynb
```

## Building the Jupyter Book

To build the book locally, ensure you have the required dependencies installed from the `requirements.txt` file. Then run:

```bash
jupyter-book build .
