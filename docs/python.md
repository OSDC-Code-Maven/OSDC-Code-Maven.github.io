# Python


## How to select a Python project to contribute to?

* For now I'll pick some of the scientific libraries. e.g. [Biology-related](https://python.code-maven.com/python-science/biology) libraries.
* Search on GitHub: [A semi-popular, recently updated Python project](https://github.com/search?q=stars%3A100..1000+pushed%3A%3E2025-10-01+language%3APython+&type=repositories&ref=advsearch) `stars:100..1000 pushed:>2025-10-01 language:Python`
* I can also ask ChatGPT to suggest other science-related libraries.
* PyDigger - once it is fixed.
* TBD

## What and how to contribute to a Python project?

* Testing
    * [Python testing demo](https://python.code-maven.com/python-testing-demo/)
    * [Python testing](https://python.code-maven.com/python-testing/)
    * Generate test coverage report
* Add type annotation
    * [Python types](https://python.code-maven.com/python-types/)
    * [Python types at PyWeb 2025.05](https://python.code-maven.com/python-types-at-pyweb-2025-05/)
* Linting
* code formatting
    * [black](https://pypi.org/project/black/)
* Fuzz testing
* Mutation testing
* code complexity analyzis
* refactoring
* Setting up CI (GitHub Actions or GitLab pipelines)
* Updating the GitHub actions if necessary
* Add [dependabot](https://docs.github.com/en/code-security/dependabot/) for GitHub Actions.
* Add dependabot for the code-base.
* Code reading


## Projects

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

## Semi specialized

* [Biopython](https://biopython.org/)

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


