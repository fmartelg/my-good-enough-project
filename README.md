# My Good Enough Project

Basic project scaffolding adapted from [good-enough-project](https://github.com/bvreede/good-enough-project) by [Barbara Vreede](https://github.com/bvreede), which is based on [Reproducible Science Cookiecutter](https://github.com/mkrapp/cookiecutter-reproducible-science) template by [Mario Krapp](https://github.com/mkrapp)

## Project setup

1. Create project folder
2. Open a terminal in your project folder and create and activate a virtual python environment.

> `python -m venv .venve`
> `.\.venv\Scripts\activate`

3. Update `pip`

> python -m pip install --upgrade pip

4. Install cookiecutter

> pip install cookiecutter

5. Scaffold project

> cookiecutter gh:fmartelg/my-good-enough-project

6. Install dev tools

> pip install pip-tools

7. Create file `requirements.in` e.g.

> pandas
> scikit-learn>=1.2

8. Compile to pinned `requirements.txt`

> pip-compile requirements.in

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
