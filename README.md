# Fast Knowledge Graph Question Answering

Our framework delivers a fast OpenIE-based knowledge extraction system and a graph-based answer prediction model for question-answering tasks. The system was designed by leveraging existing tools to accomplish a simple prototype for fast experimentation, especially across different knowledge domains, with the added benefit of reducing development time and costs.

The High level view of the proposed framework.

<p align="center">
  <img src="https://github.com/d1egoprog/FastKGQA/blob/main/images/pipeline.png?raw=true" alt="High level Pipeline"/>
</p>

## Dataset

The [MovieQA](https://metatext.io/datasets/movieqa) (a.k.a WikiMovies) dataset is a question-answering pair dataset built by Wikipedia that includes the raw source text and the corresponding KB framed in the movies domain. The original triple KB has been modified to ensure proper processing by our framework, extracting individual (S,P,O); as shown in the Figure, each original triple is split into as many triples as there are tail entities.

<p align="center">
  <img src="https://github.com/d1egoprog/FastKGQA/blob/main/images/modifiedtriples.png?raw=true" alt="Splitted Triples"/>
</p>

## Citations 

If this work is with your interest you can read the presented [paper](https://doi.org/10.3390/info14030186) and if you use it in your research please don't forget to cite 👍 this work, the suggested citation in BibTex format is:

``` BibTex
@article{DiPaolo2023,
author = {{Di Paolo}, Giuseppina and Rincon-Yanez, Diego and Senatore, Sabrina},
doi = {10.3390/info14030186},
issn = {2078-2489},
journal = {Information},
month = {mar},
number = {3},
pages = {186},
title = {{A Quick Prototype for Assessing OpenIE Knowledge Graph-Based Question-Answering Systems}},
url = {https://www.mdpi.com/2078-2489/14/3/186},
volume = {14},
year = {2023}
}
```

## Contact

If any error is found, please open an issue. The [Github repository Issues URL](https://github.com/d1egoprog/FastKGQA/issues). Contributing is always welcome. 

### Licensing

This work is published under MIT Licence.