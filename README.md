
![StataMin](https://img.shields.io/badge/stata-2011-blue) ![issues](https://img.shields.io/github/issues/asjadnaqvi/stata-tidytuesday) ![license](https://img.shields.io/github/license/asjadnaqvi/stata-tidytuesday) ![Stars](https://img.shields.io/github/stars/asjadnaqvi/stata-tidytuesday) ![version](https://img.shields.io/github/v/release/asjadnaqvi/stata-tidytuesday) ![release](https://img.shields.io/github/release-date/asjadnaqvi/stata-tidytuesday)

[Installation](#Installation) | [Examples](#Examples) | [Feedback](#Feedback) | [Change log](#Change-log)

---



# tidytuesday v1.0 (beta)
*(16 Feb 2025)*

A Stata package for fetching meta information and files from the R [TidyTuesday](https://github.com/rfordatascience/tidytuesday) challenge. 

The main purpose of this package is to give quick access to data for visualizations.

**NOTE**: A helpfile currently does not exist but the use is fairly straightforward. See below.


## Examples

Load meta data for a certain year:

```stata
tidytuesday, year(2024)
```

The meta list will give a `load` option for each week. Additional links are also provided to take users directly to the repository or other data sources.

Otherwise a specific week can be downloaded directly by specifying:

```stata
tidytuesday get, year(2025) week(3)
```

Note that each weekly challenge can contain multiple files. All of these files will be downloaded separately. Please set the path before downloading the files.

Some challenges might fail to load due to certain data formatting issues. In this case, please visit the repository directly and deal with the files on a case-by-case basis.



## Feedback

Please open an [issue](https://github.com/asjadnaqvi/stata-tidytuesday/issues) to report errors, feature enhancements, and/or other requests.


## Change log

**v1.0 (16 Feb 2025)**
- Public release.


