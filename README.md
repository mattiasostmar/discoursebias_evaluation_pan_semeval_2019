# Dataset
## Source
The labeled dataset is from [https://pan.webis.de/semeval19/semeval19-web/](https://pan.webis.de/semeval19/semeval19-web/). Access to the actual dataset can be applied for at [https://zenodo.org/record/1489920](https://zenodo.org/record/1489920).

## Download pickle-files with Pandas DataFrames
The DataFrames produced by and used in this code can be downloaded from [osf.io](https://osf.io/n2ku6/) in case you don't want to produce them yourself by running the code. It took a couple of days using one core in the Jupyter Notebooks. 

## How to reproduce
To use the code as is, create a new folder named `data` where you uncompress the files in the dataset you've gotten from the link above.

Your current folder should now look like this:

```
discoursebias_evaluation_pan_semeval_2019/
├── 1a_create_paragraphed_texts_in_pandas_dataframe_from_xml_bypublisher.ipynb
├── 1b_create_dataframe_unparagraphed_texts_from_validation_bypublisher_xml_file.ipynb
├── 1c_compare_paragraphed_vs_non-paragraphed_validation_bypublisher_texts.ipynb
├── 2_collect_ground_truth_partisanship_annotations_to_dataframe.ipynb
├── 3_compare_biasIndex_score_with_hyperpartisan_scoring.ipynb
├── data
    ├── article.xsd
    └── articles-training-byarticle-20181122.xml
    └── articles-training-bypublisher-20181122.xml
    └── ground-truth-training-byarticle-20181122.xml
    └── ground-truth-training-bypublisher-20181122.xml
    └── ground-truth-validation-bypublisher-20181122.xml
    └── ground-truth.xsd
├── LICENSE
├── README.md
├── all_bias_index_classes_results.png
└── only_biased_and_dispersed_bias_index_scores_result.png
```
Make sure you are in the root folder (this repo) and start the notebook server by running `jupyter notebook` in your terminal.

You only need to run the notebooks numbered 1a, 2 and 3, since number 1b, 1c where only to make sure that leaving paragraphs or not when parsing the xml-files didn't affect the end result.

## Evaluation results

Assuming that either "Dispersed" or "Diversified" is equivalent to `hyperpartisan = false` while "Focused" or "Biased" is equivalent to `hyperpartisan = true`:

![Dispersed/Diversified vs Focused/Biased results](all_bias_index_classes_results.png?raw=true "Dispersed/Diversified vs Focused/Biased results")

Assuming that "Dispersed" means `hyperpartisan=false` and "Biased" means `hyperpartisan=true`:

![Dispersed vs Biased results](only_biased_and_dispersed_bias_index_scores_result.png?raw=true "Dispersed vs Biased results")

## See also
An 2018 overview of the problem of measuring media bias in the cross-roads of social sciences and computer science can be found in [Automated identification of media bias in news articles: an interdisciplinary literature review](https://doi.org/10.1007/s00799-018-0261-y)
