# Zeltron AnAlysis with Python (ZAAPy)
<!-- [![PyPI](https://img.shields.io/pypi/v/nonos.svg?logo=pypi&logoColor=white&label=PyPI)](https://pypi.org/project/zaapy)
[![PyPI](https://img.shields.io/badge/requires-Python%20≥%203.8-blue?logo=python&logoColor=white)](https://pypi.org/project/zaapy)
[![Documentation Status](https://readthedocs.org/projects/zaapy/badge/?version=latest)](https://nonos.readthedocs.io/en/latest/?badge=latest)
[![pre-commit.ci status](https://results.pre-commit.ci/badge/github/asoudais/zaapy/main.svg)](https://results.pre-commit.ci/badge/github/asoudais/zaapy/main.svg)
[![Code style: black](https://img.shields.io/badge/code%20style-black-000000.svg)](https://github.com/psf/black)
[![Ruff](https://img.shields.io/endpoint?url=https://raw.githubusercontent.com/charliermarsh/ruff/main/assets/badge/v2.json)](https://github.com/charliermarsh/ruff) -->

zaapy is a 2D visualization command line tool for Zeltron. It works with h5-formatted data from Zeltron and GRZeltron

##### Data Formats

Accepted formats for the data:
GRZeltron: \*.h5
Zeltron: \*.h5


:warning: :construction: This project and documentation are under construction :construction: :warning:

## Installation

:warning: zaapy requires Python 3.8 or newer. Installation method:

```bash
$ pip install zaapy
```

## Usage

### Command line
The zaapy CLI gets its parameters from two sources:
- command line parameters
- default values

Command lines parameters take priority over default values.

To get help, run
```shell
$ zaapy --help
```

```
usage: zaapy [-h] [-dir DATADIR] [-field FIELD] [-it I1 I2 DT]
            [-vmin VMIN] [-vmax VMAX] [-cmap CMAP] [-dpi DPI]
            [-geom {cartesian, spherical}] [-d] [-log] [-range x x x x]
            [-spec SPEC] [-plane x x] [-title TITLE] [-fmt FMT]

optional arguments:
 -h,--help          show this help message and exit
 -dir DATADIR       location of output files and parameter files (default: '.')
 -field FIELD       field to plot
 -it I1,I2,DT       timesteps to plot
 -vmin VMIN         min value for colorbar
 -vmax VMAX         max value for colorbar
 -cmap CMAP         choice of colormap for the map
 -dpi DPI           image file resolution
 -geom              geometry of the simulation (choice: 'cartesian','spherical')
 -spec              species to load (default: 'electrons')
 -range             range of matplotlib window
 -plane             projection plane
 -title             name of the field in the colorbar
 -fmt               format of output image file

boolean flag:
 -log               plot the log10 of the field f, i.e. log(f)

CLI-only option:
 -d                 to display the plot, turned off if multiple timesteps to plot
 -version           display version number
```

### Python module
zaapy can be used as a python module to load and work with data from simulation done with Zeltron.
```python
from zaapy.api import GasDataSet,compute

ds=GasDataSet()

```

<!-- ```
cd existing_repo
git remote add origin https://gricad-gitlab.univ-grenoble-alpes.fr/soudaisa/python-scripts-zeltron2dspherical.git
git branch -M main
git push -uf origin main
``` -->

## Contribute

We use pre-commit hooks to format the code in order to reduce bad coding behaviour

## Support

If you face an issue or a bug (might just be a feature :wink:), please report it as an issue on this repository

<!-- ## Integrate with your tools

- [ ] [Set up project integrations](https://gricad-gitlab.univ-grenoble-alpes.fr/soudaisa/python-scripts-zeltron2dspherical/-/settings/integrations) -->


<!-- ## Test and Deploy

Use the built-in continuous integration in GitLab.

- [ ] [Get started with GitLab CI/CD](https://docs.gitlab.com/ee/ci/quick_start/index.html)
- [ ] [Analyze your code for known vulnerabilities with Static Application Security Testing(SAST)](https://docs.gitlab.com/ee/user/application_security/sast/)
- [ ] [Deploy to Kubernetes, Amazon EC2, or Amazon ECS using Auto Deploy](https://docs.gitlab.com/ee/topics/autodevops/requirements.html)
- [ ] [Use pull-based deployments for improved Kubernetes management](https://docs.gitlab.com/ee/user/clusters/agent/)
- [ ] [Set up protected environments](https://docs.gitlab.com/ee/ci/environments/protected_environments.html) -->

***

# Editing this README

When you're ready to make this README your own, just edit this file and use the handy template below (or feel free to structure it however you want - this is just a starting point!).  Thank you to [makeareadme.com](https://www.makeareadme.com/) for this template.

## Description
Let people know what your project can do specifically. Provide context and add a link to any reference visitors might be unfamiliar with. A list of Features or a Background subsection can also be added here. If there are alternatives to your project, this is a good place to list differentiating factors.

## Badges
On some READMEs, you may see small images that convey metadata, such as whether or not all the tests are passing for the project. You can use Shields to add some to your README. Many services also have instructions for adding a badge.

## Visuals
Depending on what you are making, it can be a good idea to include screenshots or even a video (you'll frequently see GIFs rather than actual videos). Tools like ttygif can help, but check out Asciinema for a more sophisticated method.

## Installation
Within a particular ecosystem, there may be a common way of installing things, such as using Yarn, NuGet, or Homebrew. However, consider the possibility that whoever is reading your README is a novice and would like more guidance. Listing specific steps helps remove ambiguity and gets people to using your project as quickly as possible. If it only runs in a specific context like a particular programming language version or operating system or has dependencies that have to be installed manually, also add a Requirements subsection.

## Usage
Use examples liberally, and show the expected output if you can. It's helpful to have inline the smallest example of usage that you can demonstrate, while providing links to more sophisticated examples if they are too long to reasonably include in the README.

## Authors and acknowledgment

## License
GNU GENERAL PUBLIC LICENSE

## Project status
Still under development
