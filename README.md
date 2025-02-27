# GitHub Classroom Plagiarism Detection

This repository contains instructions and scripts to compare student submissions for plagiarism.

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
copydetect -t <directory> -e cpp -s
```

TODO: add `-b` with boilerplate code
TODO: filter to get only latest commit before deadline
