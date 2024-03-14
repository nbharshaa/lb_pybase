# Leeds Beckett Standard Template

[![Code style: black](https://img.shields.io/badge/code%20style-black-000000.svg)](https://github.com/psf/black) 

## Background

This repository is designed to be [forked](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/working-with-forks/fork-a-repo), and in doing so provide the basic layout for the Python or MicroPython code developed within modules at Leeds Beckett University. As such it is deliberately minimal in structure, but in Python style aims for a 'batteries included' development environment. Basic templates and support is therefore provided for

* [Black](https://github.com/psf/black): our standard code formatter. Most code is read far more often than it is written, and so consistency is vital in any project of any size. This is our standard, and also the standard used 
for our own Python and MicroPython libraries.
* [MkDocs](https://www.mkdocs.org/): for documentation. Good documentation is essential in any project: even the smallest. This is our standard tool.
* [Mypy](https://mypy.readthedocs.io/en/stable/): for typing and type hints. We use type hints for our libraries and code, and this is our tool to help enforce [PEP 484](https://peps.python.org/pep-0484/) when doing so.
* [Ruff](https://github.com/astral-sh/ruff): for linting and common errors. We prefer Black for code formatting, but a good quality code linter does two jobs. For all projects it helps to identify and correct common syntax (and occasionally logic) errors. As projects get larger, and especially with multiple contributors, a good linter helps enforce consistency: which again makes it much easier to find a fix bugs.
* [pytest](https://docs.pytest.org/en/8.0.x/): as the standard test harness. All projects need some form of automated testing: pytest works well for a broad range of projects, and integrates nicely with GitHub and standard IDE's. More specialist harnesses are useful for some tasks, especially embedded Python, but this is a good starting point.

## Getting Started

Either [fork](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/working-with-forks/fork-a-repo) or clone this repository using `git` using the command

```
git clone https://github.com/dlove24/lb_pybase.git <your_repo_name>
```

For example as 

```
git clone https://github.com/dlove24/lb_pybase.git test
```

Now we need to set-up the standard Python development environment. Some IDE's will do this for you, but on the command line we need to first go into the repository you have just created. Then _inside the repository directory_ do the following

1. Set-up the Python virtual environment for the tools

    ```
    python3 -m venv .venv
    ```

2. Activate the new virtual environment, so the tools can be set-up correctly (and won't interfere with whatever is currently on the system)

   ```
   source .venv/bin/activate
   ```

3. Install the standard tools, listed above, by running

   ```
   pip install -r requirements.txt
   ```

That should complete the basic setup. We have also included links to the standard Leeds Beckett libraries, as [git submodules](https://git-scm.com/book/en/v2/Git-Tools-Submodules), and so you can _optionally_ run

   ```
   git submodule init
   ```

   followed by

   ```
   git submodule update
   ```

