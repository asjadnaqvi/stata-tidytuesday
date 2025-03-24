
![StataMin](https://img.shields.io/badge/stata-2018-blue) ![issues](https://img.shields.io/github/issues/asjadnaqvi/stata-tidytuesday) ![license](https://img.shields.io/github/license/asjadnaqvi/stata-tidytuesday) ![Stars](https://img.shields.io/github/stars/asjadnaqvi/stata-tidytuesday) ![version](https://img.shields.io/github/v/release/asjadnaqvi/stata-tidytuesday) ![release](https://img.shields.io/github/release-date/asjadnaqvi/stata-tidytuesday)

[Installation](#Installation) | [Examples](#Examples) | [Feedback](#Feedback) | [Change log](#Change-log)

---

![tidytuesday_banner_LR](https://github.com/user-attachments/assets/f996dd40-ad06-4d75-af1d-15f7cc5cb292)



# tidytuesday v1.0 (beta)
*(16 Feb 2025)*

A Stata package for fetching meta information and files from the R [TidyTuesday](https://github.com/rfordatascience/tidytuesday) repository (see also for citation guidelines and license information).

The main purpose of this package is to give quick access to interesting datasets for visualizations in Stata.

:triangular_flag_on_post: The package is still beta and may contains bugs or the full scope of error checks.

:triangular_flag_on_post: The package requires internet since it is actively parsing stable GitHub links for information. Links and paths can also break so please report them.

:triangular_flag_on_post: The package requires newer Stata versions (v17+ recommended) due to newer features in default functions.

:triangular_flag_on_post: A helpfile currently does not exist but the use is fairly straightforward. See below.



## Installation

The package can be installed via SSC or GitHub. The GitHub version, *might* be more recent due to bug fixes, feature updates etc, and *may* contain syntax improvements and changes in *default* values. See version numbers below. Eventually the GitHub version is published on SSC.


SSC (**v1.0**):

```stata
ssc install tidytuesday, replace
```

Or it can be installed from GitHub (**v1.0**):

```stata
net install tidytuesday, from("https://raw.githubusercontent.com/asjadnaqvi/stata-tidytuesday/main/installation/") replace
```

## Examples

Load the meta data for a certain year:

```stata
tidytuesday, year(2024)
```

which will display an output like this:

![image](https://github.com/user-attachments/assets/bf0ce5c1-f0cd-410a-a5b3-0a33ef7c454f)


The meta list provides a data `[Load]` link next to each week's date. Additional links are also provided to take users directly to the TidyTuesday repository and other data sources.

Data for a specific week can be downloaded as follows:

```stata
tidytuesday get, year(2023) week(48)
```

Note that each weekly challenge can contain multiple files. All of these files will be downloaded. For example, the code above is for [Dr. Who](https://github.com/rfordatascience/tidytuesday/tree/main/data/2023/2023-11-28) episodes and fetches three files. These are downloaded, parsed, cleaned, and saved separately in the backend. It is advisable to read the challenge descriptions to get more information on how the files are linked, what the unique identifiers are, etc. Note that data for some files might need further cleaning, e.g. converting string to numeric variables or formatting dates, etc.

Please also remember to set a directory path before downloading the files.

:triangular_flag_on_post: Data for some weeks might fail to load due to incompatible data structure or other data formatting issues. In this case, please visit the repository and deal with the files directly.



## Feedback

Please open an [issue](https://github.com/asjadnaqvi/stata-tidytuesday/issues) to report errors, feature enhancements, and/or other requests.


## Change log

**v1.0 (16 Feb 2025)**
- Public release.


