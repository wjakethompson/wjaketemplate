# wjaketemplate

## Overview

wjaketemplate provides a custom [pkgdown](https://pkgdown.r-lib.org)
template for my personal packages. Please don’t use it for your own
package.

This package and template were inspired by
[tidytemplate](https://github.com/tidyverse/tidytemplate).

## Templates

For all sites, ensure that `DESCRIPTION` contains:

``` R
Config/Needs/website: wjakethompson/wjaketemplate
```

### wjake

``` yaml
template:
  package: wjaketemplate
  bootstrap: 5
  
  includes:
    after_body: >
      <script data-goatcounter="https://{YOUR DOMAIN}.goatcounter.com/count" async src="https://gc.zgo.at/count.js"></script>
      
development:
  mode: auto
```

### Updating

If you’re updating from a previous pkgdown config, use the following
checklist to make sure everything is up to date:

``` md
* [ ] `usethis::use_pkgdown_github_pages()`
* [ ] Update `DESCRIPTION` to include `Config/Needs/website: wjakethompson/wjaketemplate`
* [ ] Update `_pkgdown.yml` with appropriate template above.
* [ ] Remove `strip_header: true`
* [ ] Remove algolia search, if used
* [ ] Eliminate superseded navbar customisation (`home: ~`, article re-ordering)
* [ ] Update `news` structure if needed
```
