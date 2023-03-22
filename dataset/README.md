# Modified Dataset Breafing

The MovieQA (WikiMovies) [dataset](https://metatext.io/datasets/movieqa) is a question-answering pair dataset built by Wikipedia that includes the raw source text and the corresponding KB framed in the movies domain.

However, the original triple KB has been modified to ensure proper processing by our framework, extracting the individual <subject, predicate, object>; as shown in Figure 4, each original triple is split into as many triples as there are tail entities. 

The triples reached over 376 thousand statements for the full KB, and over 134 thousand statements for the Wikipedia dataset.

<p align="center">
  <img src="https://github.com/d1egoprog/FastKGQA/blob/main/images/modifiedtriples.png?raw=true" alt="Splitted Triples"/>
</p>

## Structure

The modifications are separeted in the folders `full` and `wiki_entities` simulating the original folders from the moviesqa dataset; additionally the sufix `_splitted` was added to each of the generated files to merge easyly with the original dataset if is needed. In each folder, was created:

1. The vocabularies for the `subject` and `predicates` in separated files.
2. A single vocabulary file for the `subject` and `object` merged.
3. The complete KB is stored in a `<TAB>` separated value file in `.txt` following the `<subject><TAB><object><TAB><predicate>` for each line.

This is structure is given to be easyly imported by `tensorflow` methods.

``` PYTHON
import tensorflow as tf

file_prefix = 'full/full_kb_splitted.'

tf.flags.DEFINE_string('data_file', '{}txt'.format(file_prefix), 'data file')
tf.flags.DEFINE_string('ent_vocab', '{}entities.vocab'.format(file_prefix), 'entity vocab file')
tf.flags.DEFINE_string('rel_vocab', '{}predicates.vocab'.format(file_prefix), 'relation vocab file')

FLAGS = tf.flags.FLAGS

def _parse(line):
    """Parse train data."""
    cols_types = [[''], [''], ['']]
    return tf.decode_csv(line, record_defaults=cols_types, field_delim='\t')

dataset = tf.data.TextLineDataset(FLAGS.data_file)
dataset = dataset.map(_parse, num_parallel_calls=4)
```