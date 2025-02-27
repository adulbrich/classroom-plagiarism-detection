# GitHub Classroom Plagiarism Detection

This repository contains instructions and scripts to compare student submissions for plagiarism.

TODO:

- [ ] filter to get only latest commit before deadline

## Prerequisites

### Python and Miniconda

```shell

```

### GitHub CLI

```shell
brew install gh
gh auth login
gh extension install github/gh-classroom
```

### [Copydetect](https://github.com/blingenf/copydetect)

[Manage Environments with Conda](https://docs.conda.io/projects/conda/en/latest/user-guide/tasks/manage-environments.html)

```shell
conda create --name classroom
conda activate classroom
conda install pip
pip install copydetect
```

#### Leaving an Environment

```shell
conda deactivate
```

## Retrieve Your Student Repos

Check your assignment in GitHub Classroom, click "Download", select "Student Repositories", and copy the Classroom CLI command. 

## Running Plagiarism Detection

This command searches for plagiarism in the `<directory>`, for `cpp` extensions, and for files with the same name.

```shell
copydetect -t <directory> -e cpp -s -b <template directory>
```

## Courses

### ENGR 103 Winter 2025

Boilerplate Code / Templates (skipping assignments 1 and 2 because they were very simple):

- `gh repo clone adulbrich/engr103-financial-planner`
- `gh repo clone adulbrich/engr103-dictionary`
- `gh repo clone adulbrich/engr103-calculator`

### CS 362 Spring 2025

TBD
