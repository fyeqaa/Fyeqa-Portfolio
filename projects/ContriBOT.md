---
title: "ContriBOT"
description: Detection and extraction of Author Contribution statements and ORCID from scientific papers
image: ../images/ContriBOT.png
---
<a href="https://github.com/quest-bih/ContriBOT" target="_blank">
  <button style="background-color:#24292e; color:white; padding:8px 16px; border:none; border-radius:5px; cursor:pointer;">
    GitHub
  </button>
</a>


This project was developed in collaboration with the BIH QUEST Center for Responsible Research, where I worked as a working student focusing on text mining and scientific metadata extraction

ContriBOT is a text mining algorithm that parses a set of publications and detects which publications included Authorship Statements, Acknowledgements and ORCIDs.It is a tool that searches for typical section headings preceded by a section tag, in order to extract the author contribution and acknowledgement sections, as well as ORCID mentions. The extracted author contribution section can then be further screened and categorized, for example for following the CRediT taxonomy, or including actual author contributions


My Role

- Developed and optimized regex patterns for accurate detection of Author contributions statements and ORCID extraction
- Contributed key functionalities to the ContriBOT R package to enhance metadata extraction
- Collaborated closely with the BIH QUEST Center research team 


#### Installation

The latest version of the algorithm is structured as an R package and can easily be installed with the following command::

```r
# Install devtools if needed
# install.packages("devtools")

devtools::install_github("quest-bih/ContriBOT")
```
