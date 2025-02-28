# quantifying

Quantifying the Commons

## Overview

This project seeks to quantify the size and diversity of the commons--the
collection of works that are openly licensed or in the public domain.

## Code of Conduct

[`CODE_OF_CONDUCT.md`](CODE_OF_CONDUCT.md):
> The Creative Commons team is committed to fostering a welcoming community.
> This project and all other Creative Commons open source projects are governed
> by our [Code of Conduct][code_of_conduct]. Please report unacceptable
> behavior to [conduct@creativecommons.org](mailto:conduct@creativecommons.org)
> per our [reporting guidelines][reporting_guide].

[code_of_conduct]: https://opensource.creativecommons.org/community/code-of-conduct/
[reporting_guide]: https://opensource.creativecommons.org/community/code-of-conduct/enforcement/

## Contributing

See [`CONTRIBUTING.md`](CONTRIBUTING.md).

## Development

To set up the development environment for this project, you'll need to install [Pipenv](https://pipenv.pypa.io/) and its dependencies. Here's how to do it on Windows:

1. Install Python: If you haven't already, download and install Python from the official website: [python.org](https://www.python.org/downloads/). Make sure to check the box that says "Add Python to PATH" during the installation.

2. Install Pipenv: Open a command prompt and run the following command to install Pipenv using pip (Python package installer):

   ```shell
   pip install pipenv

   pipenv --version
   pipenv install --dev
   pipenv shell

Replace the existing Development section in the Readme.md file with this code snippet. Remember to modify it further if needed to fit the specific requirements of your project.

### Prerequisites

This repository uses [pipenv][pipenvdocs] to manage the required Python
modules:

- Linux: [Installing Pipenv][pipenvinstall]
- macOS:
  1. Install [Homebrew][homebrew]
  2. Install pipenv:

        ```install pipenv
        brew install pipenv
        ```

[pipenvdocs]: https://pipenv.pypa.io/en/latest/
[homebrew]: https://brew.sh/
[pipenvinstall]: https://pipenv.pypa.io/en/latest/install/#installing-pipenv

### Running Scripts that Require Client Credentials

To successfully run scripts that require client credentials, you will need to follow these steps:

  1. Copy the contents of the `env.example` file in the script's directory to `.env`:

        ```example
        cp env.example .env
        ```

  2. Uncomment the variables in the `.env` file and assign values as needed. See [`sources.md`](sources.md) on how to get credentials:

        ```Keys
        GOOGLE_API_KEYS=your_api_key
        PSE_KEY=your_pse_key
       ```

  3. Save the changes to the `.env` file.

  4. You should now be able to run scripts that require client credentials without any issues.

### Tooling

- **[Python Guidelines — Creative Commons Open Source][ccospyguide]**
- [Black][black]: the uncompromising Python code formatter
- [flake8][flake8]: a Python tool that glues together pep8, pyflakes, mccabe,
  and third-party plugins to check the style and quality of some Python code.
- [isort][isort]: A Python utility/library to sort imports.
- **Helper Script**  
git config --global user.name "Abhishek Anand"
git config --global user.email "<anandshek14052@gmail.com>"

  - [tools.sh](./dev/tools.sh): A useful helper script for performing specific tasks. Include a brief description of what this script does and how it can be utilized.

### Continuous Integration (CI) with GitHub Actions

- **Static Analysis**
  - [python_static_analysis.yml](.github/workflows/python_static_analysis.yml): A GitHub Action workflow for running static analysis on Python code. This workflow checks for code quality, style, and potential issues using popular tools like flake8 and isort. Provide a brief overview of how this workflow works and how to incorporate it into the development process.

[ccospyguide]: https://opensource.creativecommons.org/contributing-code/python-guidelines/
[black]: https://github.com/psf/black
[flake8]: https://gitlab.com/pycqa/flake8
[isort]: https://pycqa.github.io/isort/
git commit -s -m "Fixes #53 by @TimidRobot

Add /dev/tools.sh documentation and usage in README.md
Add .github/workflows/python_static_analysis.yml documentation in README.md"

## Data Sources

Kindly visit the [`sources.md`](sources.md) file for it.

## History

For information on past efforts, see [`history.md`](history.md).

## Copying & License

### Code

[`LICENSE`](LICENSE): the code within this repository is licensed under the Expat/[MIT][mit] license.

[mit]: http://www.opensource.org/licenses/MIT "The MIT License | Open Source Initiative"

### Data

[![CC0 1.0 Universal (CC0 1.0) Public Domain Dedication
button][cc-zero-png]][cc-zero]

The data within this repository is dedicated to the public domain under the
[CC0 1.0 Universal (CC0 1.0) Public Domain Dedication][cc-zero].

[cc-zero-png]: https://licensebuttons.net/l/zero/1.0/88x31.png "CC0 1.0 Universal (CC0 1.0) Public Domain Dedication button"
[cc-zero]: https://creativecommons.org/publicdomain/zero/1.0/

### Documentation

[![CC BY 4.0 license button][cc-by-png]][cc-by]

The documentation within the project is licensed under a [Creative Commons
Attribution 4.0 International License][cc-by].

[cc-by-png]: https://licensebuttons.net/l/by/4.0/88x31.png#floatleft "CC BY 4.0 license button"
[cc-by]: https://creativecommons.org/licenses/by/4.0/ "Creative Commons Attribution 4.0 International License"
