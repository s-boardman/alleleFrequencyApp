###Using high-resolution variant frequencies to empower clinical genome interpretation  

This web page contains a suite of tools to support the use of allele frequency information for the assessment of rare genetic variants in Mendelian disease.

Distinguishing disease-causing variants from benign bystanders is perhaps the principal challenge in contemporary clinical genetics. Rarity of an allele is widely recognized as a necessary (though not sufficient) criterion for variant pathogenicity, but the key question "*how common is too common?*" remains poorly answered for many diseases. Recent large reference datasets, such as from the [Exome Aggregation Consortium (ExAC)](exac.broadinstitute.org), provide new opportunities for robust and rigorous variant assessment.

The methods and mathematical derivations behind the calculators on these pages are described fully in our manuscript available [here](insertLink).  The source code for [the manuscript](insertlink) is available on GitHub, as is the source code for [these calculators](https://github.com/jamesware/alleleFrequencyApp).

We provide four calculators:

- `calculate AF` - works step by step through a framework of variant assessment.  For a disease of interest the user inputs parameters that describe the genetic architecture of the condition, and the calculator computes the maximum expected allele frequency of a disease-causing variant in the general population (*maximum credible population AF*). In a second step, the calculator determinues the maximum permissible allele count in a specific reference population (such as ExAC), based on the size of the population and at a user-specified confidence level.  

- `calculate AC` - performs the second part of the above work-flow, allowing the user to simply input a *maximum credible population AF* without redefining the genetic architecture in detail, intended as a time saving measure for returning users.  

- `explore architecture` - starts by computing a *maximum credible population AF* for a given genetic architecture, as above.  However, it also allows you to fix the maximum population AF in order to find a genetic architecture that is compatible with the observed data.  For example, under your initial assumptions about a condition you may find that a variant is reported to be too common, but that it would be compatible with disease under a model of substantially reduced penetrance.  

- `inverse AF` - begins with an observed allele count, and computes the highest *maximum credible population AF* for which the observed AC is compatible with pathogenicity.  This corresponds to the "filter_AF" annotation in the ExAC dataset.  ExAC returns the value for a 95% confidence - here the user can choose from a range of thresholds.


