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


### Prerequisites

This repository uses [pipenv][pipenvdocs] to manage the required Python
modules:
- Linux: [Installing Pipenv][pipenvinstall]
- macOS:
  1. Install [Homebrew][homebrew]
  2. Install pipenv:
        ```
        brew install pipenv
        ```

[pipenvdocs]: https://pipenv.pypa.io/en/latest/
[homebrew]: https://brew.sh/
[pipenvinstall]: https://pipenv.pypa.io/en/latest/install/#installing-pipenv


### Tooling

- **[Python Guidelines — Creative Commons Open Source][ccospyguide]**
- [Black][black]: the uncompromising Python code formatter
- [flake8][flake8]: a python tool that glues together pep8, pyflakes, mccabe,
  and third-party plugins to check the style and quality of some python code.
- [isort][isort]: A Python utility / library to sort imports.

[ccospyguide]: https://opensource.creativecommons.org/contributing-code/python-guidelines/
[black]: https://github.com/psf/black
[flake8]: https://gitlab.com/pycqa/flake8
[isort]: https://pycqa.github.io/isort/


### Data Sources


## CC Legal Tools

- [`legal-tool-paths.txt`](google_custom_search/legal-tool-paths.txt)
  - A `.txt` provided by Timid Robot containing all legal tool paths. The data
    from Google Custom Search will only cover 50+ general, most significant
    categories of CC License for data collection quota constraint. As an
    additional note, the order of precedence of license the collected data's
    first column is sorted due to intermediate data analysis progress.
    - [add list of all current CC legal tool paths by TimidRobot · Pull Request
      #7 · creativecommons/quantifying][pr7]

[pr7]: https://github.com/creativecommons/quantifying/pull/7


#### Google Custom Search JSON API

- The Custom Search JSON API allows user-defined detailed query and access
  towards related query data using a programmable search engine.
  - [Custom Search JSON API Reference | Programmable Search Engine | Google
    Developers][googlejsonapi]
  - [Method: cse.list | Custom Search JSON API | Google Developers][cselist]
- [`google_countries.tsv`](google_custom_search/google_countries.txt)
  - Created by directly copy and pasting the `cr` parameter list from the
    following link into a `.tsv` file as there were no reliable algorithmic way
    for retrieving such data found in the process so far. The script itself
    will take care of the formatting and country-selection process.
    - [Country Collection Values | JSON API reference | Programmable Search
      Engine | Google Developers][googlecountry]
- [`google_lang.txt`](google_custom_search/google_lang.txt)
  - Created by directly copy and pasting the `lr` parameter list from the
    following link into a `.txt` file as there were no reliable algorithmic way
    for retrieving such data found in the process so far. The script itself
    will take care of the data formatting and language-selection process.
    - [Parameter: lr | Method: cse.list | Custom Search JSON API | Google
      Developers][googlelang]

[googlejsonapi]: https://developers.google.com/custom-search/v1
[cselist]: https://developers.google.com/custom-search/v1/reference/rest/v1/cse/list
[googlecountry]: https://developers.google.com/custom-search/docs/json_api_reference#countryCollections
[googlelang]: https://developers.google.com/custom-search/v1/reference/rest/v1/cse/list#body.QUERY_PARAMETERS.lr


## Internet Archive Python Interface

A python interface to archive.org to achieve API requests towards internet
archive.
- [`internetarchive.Search` - Internetarchive: A Python Interface to
  archive.org][iasearch]

[iasearch]: https://internetarchive.readthedocs.io/en/stable/internetarchive.html#internetarchive.Search


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
