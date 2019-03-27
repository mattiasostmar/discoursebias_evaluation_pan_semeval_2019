# Dataset
## Source
The labeled dataset is from [https://pan.webis.de/semeval19/semeval19-web/](https://pan.webis.de/semeval19/semeval19-web/). Access to the actual dataset can be applied for at [https://zenodo.org/record/1489920](https://zenodo.org/record/1489920).

## Download pickle-files with Pandas DataFrames
The DataFrames produced by and used in this code can be downloaded from [osf.io](https://osf.io/n2ku6/) in case you don't want to produce them yourself by running the code. It took a couple of days using one core in the Jupyter Notebooks. 

## Evaluation results

Assuming that either "Dispersed" or "Diversified" is equivalent to `hyperpartisan = false` while "Focused" or "Biased" is equivalent to `hyperpartisan = true`:

![Dispersed/Diversified vs Focused/Biased results](all_bias_index_classes_results.png?raw=true "Dispersed/Diversified vs Focused/Biased results")

Assuming that "Dispersed" means `hyperpartisan=false` and "Biased" means `hyperpartisan=true`:

![Dispersed vs Biased results](only_biased_and_dispersed_bias_index_scores_result.png?raw=true "Dispersed vs Biased results")

## See also
An 2018 overview of the problem of measuring media bias in the cross-roads of social sciences and computer science can be found in [Automated identification of media bias in news articles: an interdisciplinary literature review](https://doi.org/10.1007/s00799-018-0261-y)