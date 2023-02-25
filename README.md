# Fast Knowledge Graph Question Answering

Our framework delivers a fast OpenIE-based knowledge extraction system and a graph-based answer prediction model for question-answering tasks. The system was designed by leveraging existing tools to accomplish a simple prototype for fast experimentation, especially across different knowledge domains, with the added benefit of reducing development time and costs.

The High level view of the proposed framework.

<p align="center">
  <img src="https://github.com/d1egoprog/FastKGQA/blob/main/images/pipeline.png?raw=true" alt="High level Pipeline"/>
</p>

## Dataset

The [MovieQA](ttps://metatext.io/datasets/movieqa) (a.k.a WikiMovies) dataset is a question-answering pair dataset built by Wikipedia that includes the raw source text and the corresponding KB framed in the movies domain. The original triple KB has been modified to ensure proper processing by our framework, extracting individual (S,P,O); as shown in the Figure, each original triple is split into as many triples as there are tail entities.

<p align="center">
  <img src="https://github.com/d1egoprog/FastKGQA/blob/main/images/modifiedtriples.png?raw=true" alt="Splitted Triples"/>
</p>

## Citations 

If this work is with your interest you can read the presented [paper]() and if you use it in your research please don't forget to cite 👍 this work, the suggested citation in BibTex format is:

``` BibTex
@article{Di-Paolo2023,
  title={A quick prototype for assessing OpenIE Knowledge Graph-based question-answering systems},
  author = {Di-Paolo, Giuseppina and Rincon-Yanez, Diego and Senatore, Sabrina},
  journal={TBD},
  volume={TBD},
  number={TBD},
  pages={17},
  year={2023},
  doi = {TBD},
  publisher={TBD}
}
```

## Contact

If any error is found, please open an issue. The [Github repository Issues URL](https://github.com/d1egoprog/FastKGQA/issues). Contributing is always welcome. 

### Licensing

This work is published under MIT Licence.