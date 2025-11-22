---
{"dg-publish":true,"dg-path":"Coding/use tidyverse to wrangle data.md","permalink":"/coding/use-tidyverse-to-wrangle-data/","tags":["Reference"],"updated":"2025-09-30"}
---


#### Core tidyverse comprised of 9 key packages i.e. dplyr, tibble, ggplot2, readr, tidyr, stringr, forcats, lubridate, and purr
- `tidyr` is to help you create a tidy data.
	- [Tidy Messy Data • tidyr (tidyverse.org)](https://tidyr.tidyverse.org/)
		- it supersedes `reshape2` library
	- The key functions offered by this package are `pivot_longer`, `pivot_wider`, `nest`, `unnest`. Other useful functions are `separate`, `extract` and `unite` for manipulating character columns.
		- `unnest_` is meant to turns nested list into tidy tibbles.
- `dplyr` is for data manipulation and practically the biggest library (has the most functions)
	- [A Grammar of Data Manipulation • dplyr (tidyverse.org)](https://dplyr.tidyverse.org/)
		- providing a consistent set of verbs that help you solve the most common data manipulation challenges:
	- The key functions offered by this package are `mutate`, `select`, `filter`, `summarise`, `arrange`, and `group_by`. However, the functions I usually use are the following
		- To manage columns: `glimpse`, `mutate`, `rename_with`, and `select`
		- To manage data frames: `bind_cols`, `bind_rows`, `left_join`
- `readr` provides a fast and friendly way to read rectangular data (like csv, tsv, and fwf)

#### One of the non-core tidyverse package that I use are magrittr that provide simple forward-pipe operator for R
- The package is part of the `install.packages("tidyverse")` installation. But I can install just itself with `install.packages("magrittr")`. See [A Forward-Pipe Operator for R • magrittr](https://magrittr.tidyverse.org/) for more details. Example usage as per code block below
- Base R since version 4.1.0 have also introduced forward-pipe but with the connotation `|>` (instead of `magrittr` that use `%>%`)

```
mtcars %>%
  group_by(cyl, vs) %>%
  summarise(cyl_n = n()) %>%
```

## References
- [Tidyverse packages](https://www.tidyverse.org/packages/)