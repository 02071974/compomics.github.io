---
name: 3InstructionstorunCLIfortheidentificationofcrosslinkedpeptides
project: xilmass
layout: default
permalink: /projects/xilmass/wiki/3instructionstorunclifortheidentificationofcrosslinkedpeptides.html
github_project: https://github.com/compomics/xilmass
---

**1-** Update the configuration file (xLink.properties) according to your search settings.
<br> 
 Detailed information on the different parameters can be found on [here] (https://github.com/compomics/xilmass/wiki/3.1.-Xilmass-parameters-CLI).
 
<br>
**2-** Make sure that your database contains both target and decoy sequences with generic headers.
<br> You can use [DBToolKit] (/projects/dbtoolkit.html) to generate your decoy database. Every decoy must contain either `_REVERSED` or `_SHUFFLED` next to the accession number position at its header. For example, one target header of `PXXX` has its decoy which is either `PXXX_REVERSED` or `PXXX_SHUFFLED` 
<br> For details, please see [5. Database](https://github.com/compomics/xilmass/wiki/5.-Database). 

<br>
**3-** In order to run Xilmass, execute the following line on the command prompt
>java –jar xilmass.X.Y.Z.jar -c 

<br> Note that X.Y.Z stands for version number.

After running Xilmass, there will be a fastacp file on the given cxDBName. This search database is composed  of all possible generated cross-linked peptides. The details on the presentation of this cross-linked peptide database can be found on [here](https://github.com/compomics/xilmass/wiki/5.-Database). There will be an output folder that is set by a user. In this folder, there are Xilmass outputs for ever mgf file, one file that contains validated cross-linked peptides-to-spectrum matches (XPSMs), one file that contains all XPSMs and one file for search settings. 
