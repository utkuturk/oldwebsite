---
layout: "post"
---


Using [this query][1] as a reference, I found a way to get R to parse the config file as an R expression.  My config files now read:

    experiments:
      # Config paths
      first: !expr 'paste0("C:/Users/",Sys.info()[6], "/OneDrive/Science/experiments/first")'
      second: !expr 'paste0("C:/Users/",Sys.info()[6], "/OneDrive/Science/experiments/second")'
      third: ...

Then, when I read it in R, I use `config = yaml::read_yaml('base/config.yaml', eval.expr=TRUE)` and it works perfectly.  It feels like a fragile solution, but so far it's holding up.


  [1]: https://stackoverflow.com/questions/64454623/r-read-yaml-reads-a-vector-as-parameter