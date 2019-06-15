<a href="http://www.europeana-newspapers.eu/"><img src=http://www.europeana-newspapers.eu/wp-content/uploads/2013/09/europeana_newspapers_forwebsite1.jpg></a> 

### ner-corpora
Named Entity Recognition corpus for (historical) Dutch, French and German from [Europeana Newspapers](http://www.europeana-newspapers.eu/named-entity-recognition-for-digitised-newspapers/).

### Introduction

The corpus comprises of one tsv file per language following the [GermEval2014](https://sites.google.com/site/germeval2014ner/data) data format. The format is a simple tab-separated-values format that divides texts into single tokens per line with tab-separated annotations. The 1st column contains the token position in the sentence. The 2nd column contains  the token itself. The third column contains the named entity annotation. The fourth column can contain an embedded named entity annotation. Sentence boundaries are indicated with new lines, comments start with ```#```.

The most commonly used categories for tags are ```PER``` (person), ```LOC``` (location) and ```ORG``` (organization) with a prefix of either ```B-``` (beginning of named entity) or ```I-``` (inside of named entity). ```O``` (outside of named entity) is used for tokens that are not a named entity.

Example:
```
# This is an example
1 The O O
2 NBA B-ORG O
3 player  O O
4 Michael B-PER O
5 Jordan  I-PER O
6 is  O O
7 not  O O
8 the O O
9 President B-PER O
10  of  I-PER O
11  the I-PER O
# next we see the embedding structure
12  United  I-PER B-LOC
13  States  I-PER I-LOC
14  of  I-PER I-LOC
15  America I-PER I-LOC
16  . O O
```

### Background

The tsv files in this repository are based on digitized and OCRed historical newspapers sourced from these libraries:

* [enp_DE](https://github.com/EuropeanaNewspapers/ner-corpora/tree/master/enp_DE.onb.tsv) - newspapers from the [Austrian National Library](http://www.theeuropeanlibrary.org/tel4/newspapers/gallery?provider-id=P01252), [Berlin State Library](http://www.theeuropeanlibrary.org/tel4/newspapers/gallery?provider-id=P01606) and [Dr Friedrich Teßmann Library](http://www.theeuropeanlibrary.org/tel4/newspapers/gallery?provider-id=P02013)
* [enp_FR](https://github.com/EuropeanaNewspapers/ner-corpora/tree/master/enp_FR.bnf.tsv) - newspapers from the [National Library of France](http://www.theeuropeanlibrary.org/tel4/newspapers/gallery?provider-id=P01190)
* [enp_NL](https://github.com/EuropeanaNewspapers/ner-corpora/tree/master/enp_NL.kb.tsv) - newspapers from the [National Library of the Netherlands](http://www.theeuropeanlibrary.org/tel4/newspapers/gallery?provider-id=P01350)

### License 

[CC0](https://creativecommons.org/publicdomain/zero/1.0/)

### Attribution 

*Europeana Newspapers NER corpora*       
*https://github.com/EuropeanaNewspapers/ner-corpora/*    
*Europeana Newspapers Project, 2012-2015*     
*http://www.europeana-newspapers.eu/*   

### References

* [An Open Corpus for Named Entity Recognition in Historic Newspapers](http://www.lrec-conf.org/proceedings/lrec2016/summaries/110.html)  
Proceedings of the 10th edition of the Language Resources and Evaluation Conference (LREC 2016), 23-28 May 2016, Portorož, Slovenia.

### Known issues

The way the above corpora were produced, additional work is required to leverage the data for tasks such as evaluation, where gold standard quality is required as the data still contains many OCR errors. Further information on data quality issues and instructions to clean up the data can be found in the [wiki](https://github.com/EuropeanaNewspapers/ner-corpora/wiki).
