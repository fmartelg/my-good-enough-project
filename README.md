# My Good Enough Project

Basic project scaffolding adapted from [good-enough-project](https://github.com/bvreede/good-enough-project) by [Barbara Vreede](https://github.com/bvreede), which is based on [Reproducible Science Cookiecutter](https://github.com/mkrapp/cookiecutter-reproducible-science) template by [Mario Krapp](https://github.com/mkrapp)

## Project setup

1. Open projects folder and use cookiecutter installed in base distribution to create a new project folder and scaffolding.

   `cd C:\Projects`
   `cookiecutter gh:fmartelg/my-good-enough-project`

2. Change to the project folder and create and activate a virtual python environment.

   `cd C:\Projects\mynewproj`  
   `python -m venv .venv`  
   `.\.venv\Scripts\activate`

3. Initialize Git repo

   `git init`

4. Update pip and install dev tools

   `python.exe -m pip install --upgrade pip`  
   `pip install pip-tools`

5. Create file `requirements.in` e.g.

   `pandas`  
   `scikit-learn>=1.2`

6. Compile to pinned `requirements.txt`

   `pip-compile requirements.in`

7. Install requirements

   `pip-sync requirements.txt`

## Project Structure

The project structure distinguishes three kinds of folders:

- read-only (RO): not edited by either code or researcher
- human-writeable (HW): edited by the researcher only.
- project-generated (PG): folders generated when running the code; these folders can be deleted or emptied and will be completely reconstituted as the project is run.

```text
.
├── .gitignore
├── CITATION.md
├── LICENSE.md
├── README.md
├── requirements.txt
├── bin                <- Compiled and external code, ignored by git (PG)
│   └── external       <- Any external source code, ignored by git (RO)
├── config             <- Configuration files (HW)
├── data               <- All project data, ignored by git
│   ├── processed      <- The final, canonical data sets for modeling. (PG)
│   ├── raw            <- The original, immutable data dump. (RO)
│   └── temp           <- Intermediate data that has been transformed. (PG)
├── docs               <- Documentation notebook for users (HW)
│   ├── manuscript     <- Manuscript source, e.g., LaTeX, Markdown, etc. (HW)
│   ├── notes          <- Project notes (HW)
│   ├── ref            <- Reference documents, e.g terms of reference, background docs, etc. (HW)
│   └── reports        <- Other project reports and notebooks (e.g. Jupyter, .Rmd) (HW)
├── results
│   ├── figures        <- Figures for the manuscript or reports (PG)
│   └── output         <- Other output for the manuscript or reports (PG)
└── src                <- Source code for this project (HW)
```

## License

This project is licensed under the terms of the [MIT License](/LICENSE.md).
