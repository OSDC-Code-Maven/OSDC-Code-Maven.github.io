# Python

* [Events](#events)
* [Chat](#chat)
* [How to select a Python project to contribute to?](#how-to-select-a-python-project-to-contribute-to)
* [What and how to contribute to a Python project?](#what-and-how-to-contribute-to-a-python-project)
* [Project reports](#project-reports)

## Events

This material is being used during the online events organized in the [Code-Mavens](https://www.meetup.com/code-mavens/) Meetup group.


## Chat

* [OSDC Zulip](https://osdc.zulipchat.com/)

## How to select a Python project to contribute to?

* Pick a Python-based project you use.
* Pick a Python module that your code directly depends on. They are listed in `requirements.txt` or `pyproject.toml`.
* Pick a Python module that your code indirectly depends on. They are listed in `constraints.txt`, `uv.lock`.
* Search on GitHub: [A semi-popular, recently updated Python project](https://github.com/search?q=stars%3A100..1000+pushed%3A%3E2025-10-01+language%3APython+&type=repositories&ref=advsearch) `stars:100..1000 pushed:>2025-10-01 language:Python`
* For now I'll pick some of the scientific libraries. e.g. [Biology-related](https://python.code-maven.com/python-science/biology) libraries.
* Ask ChatGPT to suggest other science-related libraries.
* Pick a popular project and work on stale PRs. That is PRs where there is already good work, but the original author (of the PR) has vanished.
* [PyDigger](https://pydigger.code-maven.com/) - once it is fixed.

## What and how to contribute to a Python project?

* Link to VCS: Does the project listing in [Pypi](https://pypi.org/) link to its public VCS? If not, try to find the VCS and the first PR could be adding this link. If you can't find the VCS then the rest will be rather irrelevant. Maybe send an email to the author asking if there is a public VCS?
* Testing: Try to run the tests locally or better yet in a [Docker conatiner](https://github.com/szabgab/python-docker-on-ubuntu).
    * [Python testing demo](https://python.code-maven.com/python-testing-demo/)
    * [Python testing](https://python.code-maven.com/python-testing/)
    * Generate test coverage report
* CI
    * If there are tests, check if there is a CI?
    * Setting up CI: GitHub Actions or GitLab pipelines.
    * Updating the GitHub actions if necessary.
* Dependencies
    * Add [dependabot](https://docs.github.com/en/code-security/dependabot/) for GitHub Actions and for the dependencies.
* Code formatting
    * Using [black](https://pypi.org/project/black/) check if the code is well formatted. If not open an issue suggestion to do it. `black --check .`
    * See also [autopep8](https://pypi.org/project/autopep8/).
* Linting
    * Run one or more linters on the code. Add, linter configuration to the project. Setup CI to run the linter(s).
    * [Pylint](https://www.pylint.org/)
    * [Flake8](https://flake8.pycqa.org/)
    * [ruff](https://astral.sh/ruff)
    * [PyChecker](https://pychecker.sourceforge.net/)
    * [Pylama](https://klen.github.io/pylama/)
    * [Sonar](https://www.sonarsource.com/knowledge/languages/python/)?
    * [Codacy](https://www.codacy.com/quality)?
* Add type annotation
    * Start by running one of the type-checking tools on the code-base. Add configurations to the repository. Setup CI to run the type-checker.
    * [mypy](https://mypy.readthedocs.io/)
    * [pytype](https://google.github.io/pytype/)
    * [Python types](https://python.code-maven.com/python-types/)
    * [Python types at PyWeb 2025.05](https://python.code-maven.com/python-types-at-pyweb-2025-05/)
* Fuzz testing
    * [atheris](https://github.com/google/atheris)
* Mutation testing
    * [mutatest](https://mutatest.readthedocs.io/)
    * [mutmut](https://github.com/boxed/mutmut)
    * [MutPy](https://pypi.org/project/MutPy/)
* Code complexity analyzis
    * [code-complexity-analyzer](https://pypi.org/project/code-complexity-analyzer/)
    * [complexipy](https://github.com/rohaquinlop/complexipy)
* Refactoring
* Code reading
* Convert `setup.py` to `pyproject.toml`.


## Project reports

* [qrcode-pretty](https://pypi.org/project/qrcode-pretty/)
    * 2026.02.03
    * PR: [added test for generated images](https://github.com/mrinfinidy/qrcode-pretty/pull/1) by nnguyen-cs (Ted) - Waiting 🕰️
    * [Video recordings](https://python.code-maven.com/adding-tests-to-qrcode-pretty-video) 🎦
    * PR: [Add the GitHub Actions to run the test on every push](https://github.com/mrinfinidy/qrcode-pretty/pull/2) by nnguyen-cs (Ted) - Waiting 🕰️
    * [Video recordings](https://python.code-maven.com/adding-github-action-to-qrcode-pretty-video) 🎦

* [factpages-py](https://pypi.org/project/factpages-py/)
    * 2026.01.20
    * Issue: [Readme has some slightly confusing info](https://github.com/kkollsga/factpages-py/issues/1) - Closed ✅
    * PR: [Add some tests based on the documentation](https://github.com/kkollsga/factpages-py/pull/2) - Merged ✅
    * Learn: [build](https://pypi.org/project/build/) A simple, correct Python build frontend.
    * Learn: [twine](https://pypi.org/project/twine/) a utility for publishing Python packages on PyPI.
    * 2026.01.23
    * We used the Docker container to get test coverage:
    * `pip install pytest-cov`
    * `pytest --cov=factpages_py --cov-report html --cov-branch`
    * It is 24%
    * We tried to call the `field_summary` method in `analysis.py` without success.
    * Issue: [How to call field_summary in analysis.py ?](https://github.com/kkollsga/factpages-py/issues/3) - Implemented ✅
    * Add more tests - TODO 🎁

* [scikit-learn](https://scikit-learn.org/)
    * 2026.01.11
    * Setting up the development environment is [explained well](https://scikit-learn.org/dev/developers/development_setup.html) but still takes time.
    * Also running the tests took 10 minutes on my computer.
    * Maybe create a development environment in a Docker image and share the instructions how to use it.
    * Maybe describe how to use `uv` to setup the development environment.
    * Issue: [confusion_matrix crashes when sample_weight is an empty array](https://github.com/scikit-learn/scikit-learn/issues/33040) - we tried to reproduce it and commented on it. - Issue closed. ✅
    * We opened a few issues on the PyDigger project.

* readanybook
    * We encountered this project, but we could not find its GitHub repository. Someone mentioned that it might be related to some pirated books.
    * I don't know, but apparently one has to be carefull not to contribute to some illegal activity.

* [paperpipe](https://pypi.org/project/paperpipe/)
    * 2026.01.11
    * PR: [Add Dependabot configuration for version updates](https://github.com/hummat/paperpipe/pull/2) - Merged ✅
    * Check test coverage and add tests - TODO 🎁

* [peelee](https://pypi.org/project/peelee/)
    * 2026.01.11
    * I have sent an email to [Bruce Wen (wenijinew)](https://github.com/wenijinew) the author. - Waiting 🕰️

* [fastapi-cachex](https://pypi.org/project/fastapi-cachex/)
    * 2026.01.09
    * PR: [Add Dependabot configuration for version updates](https://github.com/allen0099/FastAPI-CacheX/pull/3) - Merged ✅

* [vcsp-guard](https://pypi.org/project/vcsp-guard/)
    * 2025.12.27
    * PR: [add link to github](https://github.com/Giordano10/VCSP/pull/1) - Merged ✅
    * PR: [add dependabot](https://github.com/Giordano10/VCSP/pull/2) - Closed but implemented 🤔
    * Issue: [Local development, how to run the tests locally](https://github.com/Giordano10/VCSP/issues/3) -  ✅
    * Learn: [semgrep](https://semgrep.dev/)
    * Learn: [cliff](https://github.com/orhun/git-cliff-action)
    * Learn: [build](https://pypi.org/project/build/)
    * Learn: [bandit](https://pypi.org/project/bandit/)
    * Learn: [pip-audit](https://pypi.org/project/pip-audit/)
    * Learn: [stefanzweifel/git-auto-commit-action](https://github.com/stefanzweifel/git-auto-commit-action)
    * Learn: [softprops/action-gh-release](https://github.com/softprops/action-gh-release)
    * Learn: [pypa/gh-action-pypi-publish](https://github.com/pypa/gh-action-pypi-publish)

* [conventional-pre-commit](https://github.com/compilerla/conventional-pre-commit)
    * 2025.11.20
    * [git/COMMIT_EDITMSG: error Subject should be capitalized but found chore:](https://github.com/compilerla/conventional-pre-commit/issues/142) - TODO 🎁

* [Biopython](https://biopython.org/)
    * 2025.10.24
    * [Add type annotations](https://github.com/biopython/biopython/pull/5087) - TODO 🎁
    * [chore: add type annotation to Bio/File.py](https://github.com/biopython/biopython/pull/5088) - TODO 🎁

* [MoreBeautifulPython](https://github.com/sudongqi/MoreBeautifulPython)
    * 2022.12.01
    * Article: [Test and CI for MoreBeautifulPython](https://dev.to/szabgab/day-1-test-and-ci-for-morebeautifulpython-bn8)
    * PR: [Add a simple test and set up GitHub action to run it one every push](https://github.com/sudongqi/MoreBeautifulPython/pull/2) - Merged ✅

* [farmworld](https://pypi.org/project/farmworld/)
    * 2022.12.03
    * Article: [CI for farmworld, a Python package - a failed attempt](https://dev.to/szabgab/day-3-ci-for-farmworld-a-python-package-a-failed-attempt-9dm)
    * I sent a PR, but I don't know what happened to it as the project was removed from GitHub. ❓
    * I still have my [fork](https://github.com/szabgab/farmworld) 🍴 (there is no stand-alone fork emoji)

* [wsblib](https://github.com/firlast/wsblib) - Web Server Base Library.
    * 2022.12.03
    * Article: [GitHub Action CI for wsblib Python](https://dev.to/szabgab/day-3-v2-github-action-ci-for-wsblib-python-3o9b)
    * PR: [Add GitHub Actions](https://github.com/firlast/wsblib/pull/3) - Merged ✅

* [col-spanish](https://github.com/sergioasb8/col-spanish) - A collection of tools to work with text write in Spanish (Colombia)
    * 2022.12.04
    * Article: [GitHub Actions for Colombian Spanish](https://dev.to/szabgab/day-4-github-actions-for-columbian-spanish-kop)
    * PR: [Add GitHub Actions](https://github.com/sergioasb8/col-spanish/pull/1) - Rejected ❌ without explanation.

* [pcr_optimizer](https://github.com/Ara101/pcr_optimizer/) - A Python package to aid researchers in optimizing pcr protocols (Polymerase chain reaction)
    * 2022.12.06
    * Article: [GitHub Actions CI for the pcr_optimizer Python package](https://dev.to/szabgab/day-6-github-actions-ci-for-the-pcroptimizer-python-package-441n)
    * PR: [Add GitHub Actions](https://github.com/Ara101/pcr_optimizer/pull/4) - Merged ✅

* [sdk-py](https://github.com/dimchat/sdk-py) - Decentralized Instant Messaging (Python SDK)
    * 2022.12.12
    * Article: [CI for sdk-py Python packages](https://dev.to/szabgab/ci-for-sdk-py-python-packages-1ab2)
    * PR: [Add GitHub Action](https://github.com/dimchat/sdk-py/pull/1) - Waiting 🕰️

* [core_curate_app](https://github.com/usnistgov/core_curate_app) - Curation functionalities for the curator core project.
    * 2022.12.13
    * Article: [CI for a Python project of the National Institute of Standards and Technology](https://dev.to/szabgab/ci-for-a-python-project-of-the-national-institute-of-standards-and-technology-3fic)
    * PR: [Add GitHub Actions](https://github.com/usnistgov/core_curate_app/pull/8) - Rejected ❌ without explanation.

* [vfxpaths](https://github.com/VFXToolkits/vfxpaths) - A system analysis framework related to VFX common file operations.
    * 2022.12.15
    * Article: [Failing CI to help fixing filesystem issues in a Python package](https://dev.to/szabgab/day-15-failing-ci-to-help-fixing-filesystem-issues-in-a-python-package-4p5i)
    * PR: [Add GitHub Action](https://github.com/VFXToolkits/vfxpaths/pull/6) - Merged ✅


## Some python projects

(Not fully categorized yet)

## Generic

* requests
* jupyter
* flask
* pandas
* pytest
* numpy


* allensdk
* box2d
* cv2
* deeplabcut
* functools
* glob
* gseapy
* h5py
* itertools
* joblib
* keras
* matplot
* matplotlib
* mayavi
* openpyxl
* PIL
* pygame
* pyppt
* ray
* redirect
* scipy
* seaborn
* skimage
* statsmodels
* tifffile
* voila

## ML

* scikit-fmm
* sklearn
* [tensorflow](https://www.tensorflow.org/)

## Generic visualization

* [plotly](https://plotly.com/python/)
* [bokeh](https://bokeh.org/)


## Specialized

* [pcr_optimizer](https://github.com/Ara101/pcr_optimizer/)
* [GalSim](https://github.com/GalSim-developers/GalSim) is open-source software for simulating images of astronomical objects
* [farmworld](https://github.com/tomgrek/farmworld)

* [logomaker](https://logomaker.readthedocs.io/en/latest/)
* [BCAWT](https://pypi.org/project/BCAWT/) Automated tool for codon usage bias analysis for molecular evolution
* [An-Open-Source-Computational-Tool-for-Measuring-Bacterial-Biofilm-Morphology-and-Growth-Kinetics](https://github.com/cohenoa/An-Open-Source-Computational-Tool-for-Measuring-Bacterial-Biofilm-Morphology-and-Growth-Kinetics)
* [MaLiAmPi](https://github.com/jgolob/maliampi) Maximum Likelihood Amplicon Pipeline: An amplicon (PCR / 16S) microbiome pipeline.

These 3 try to solve the same problem:

* [Bio.SeqUtils.CodonUsage module](https://biopython.org/docs/1.75/api/Bio.SeqUtils.CodonUsage.html)
* [CAI](https://cai.readthedocs.io/en/latest/) Python Codon Adaptation Index
* [Codon-Usage-in-Python](https://github.com/rhondene/Codon-Usage-in-Python)


