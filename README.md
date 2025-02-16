
![StataMin](https://img.shields.io/badge/stata-2011-blue) ![issues](https://img.shields.io/github/issues/asjadnaqvi/stata-tidytuesday) ![license](https://img.shields.io/github/license/asjadnaqvi/stata-tidytuesday) ![Stars](https://img.shields.io/github/stars/asjadnaqvi/stata-tidytuesday) ![version](https://img.shields.io/github/v/release/asjadnaqvi/stata-tidytuesday) ![release](https://img.shields.io/github/release-date/asjadnaqvi/stata-tidytuesday)

[Installation](#Installation) | [Examples](#Examples) | [Feedback](#Feedback) | [Change log](#Change-log)

---



# tidytuesday v1.0 (beta)
*(16 Feb 2025)*

A Stata package for fetching meta information and files from the R [TidyTuesday](https://github.com/rfordatascience/tidytuesday) challenge. 

The main purpose of this package is to give quick access to data for visualizations.

**NOTE**: A helpfile currently does not exist but the use is fairly straightforward. See below.


## Installation

The package can be installed via SSC or GitHub. The GitHub version, *might* be more recent due to bug fixes, feature updates etc, and *may* contain syntax improvements and changes in *default* values. See version numbers below. Eventually the GitHub version is published on SSC.


SSC (**xxx**):

```stata
COMING SOON!
```

```stata
net install tidytuesday, from("https://raw.githubusercontent.com/asjadnaqvi/stata-tidytuesday/main/installation/") replace
```

## Examples

Load the meta data for a certain year:

```stata
tidytuesday, year(2024)
```

The meta list also provides a `[Load]` link next to each date for fetching the data. Additional links are also provided to take users directly to the repository or other data sources.

Otherwise a specific week can be downloaded directly as follows:

```stata
tidytuesday get, year(2023) week(48)
```

Note that each weekly challenge can contain multiple files. All of these files will be downloaded separately. Please set the path before downloading the files.


For example, the code above is a dataset of [Dr. Who](https://github.com/rfordatascience/tidytuesday/tree/main/data/2023/2023-11-28) episodes and contains three files. It is advisable to read the challenge descriptions to get more information on how the files are linked.

**NOTE**: Data for some weeks might fail to load due to data structure or formatting issues. In this case, please visit the repository directly and deal with the files directly.



## Feedback

Please open an [issue](https://github.com/asjadnaqvi/stata-tidytuesday/issues) to report errors, feature enhancements, and/or other requests.


## Change log

**v1.0 (16 Feb 2025)**
- Public release.


