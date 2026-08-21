# Introduction to Big Data

Hands-on Python, NumPy, pandas, SQL, statistics, visualization, and machine-learning notebooks for a first- and second-year undergraduate course.

## Start here

- [Environment setup for Linux](01-0_Introduction/001_environment_setup_for_linux.md)
- [Environment setup for Windows, WSL, and Ubuntu](01-0_Introduction/002_environment_setup_for_windows_wsl_ubuntu.md)
- [Environment setup for macOS](01-0_Introduction/003_environment_setup_for_macos.md)
- [GitHub: download and update the course files](01-0_Introduction/004_github_download_and_update.md)

The numbered course chapters run from `01-1_Python_Basics_I` through `12-2_Model_Validation_and_Evaluation`. Each lesson is a stand-alone Jupyter notebook, and the examples introduce Python and data-analysis ideas in sequence. In `02-2_Data_Structures`, start with `01_data_structures_for_data_science`; the remaining notebooks are optional extensions.

## Run a lesson

```bash
source .venv/bin/activate
jupyter lab
```

Open a lesson's `.ipynb` file and run its cells in order. Data-dependent lessons use their nearby `input/` and `output/` folders when run from this repository. The collection unit includes documented API, CSV, HTML scraping, and bounded-crawling examples; live requests are optional and must follow each site's terms, rate limits, robots guidance, and license.

The notebooks are also designed for the JSPCV Playground. Generated browser files are temporary, so download any output that should be retained.
