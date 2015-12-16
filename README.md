# Contributing to Open Biomedical Corpora

First, thank you for your interest in Open Biomedical Corpora (OBC)!

OBC is an openly developed repository of manually annotated corpora created by a large community, and its success critically depends on your contribution. We warmly welcome contributions of annotated corpora, metadata on these resources, additions and corrections to documentation, and more. These instructions (work in progress) provide a few guidelines that we'd like to ask you to follow to make it easy for everyone to work on and use this shared repository.

## Adding new corpora

Before adding a new corpus to the collection, please make sure that it meets the OBC requirements (TODO link), in particular

1. **Open annotations**: The annotations in OBC resources must be available for anyone to use for any purpose without constraints other than preserving provenance and openness. (See [The Open Definition](http://opendefinition.org/), [Definition of Free Cultural Works](http://freedomdefined.org/))
2. **Accessible texts**:  The texts annotated by OBC resources must be readily accessible to anyone.

To add a new corpus, create a new GitHub repository in <http://github.com/openbiocorpora>. (You need to be a member of the OBC GitHub organization for this, please write Sampo to get added.)

For consistency, repository names should be all lower-case with dashes for space (e.g. `bionlp-st-2011-ge`).

### Repository structure

Each corpus repository in <http://github.com/openbiocorpora> should have the following top-level structure:

- `README`: Brief description of the corpus
- `LICENSE`: The corpus license
- `SOURCE`: List of URLs for corpus data
- `original-data/`: Directory with corpus data

The `original-data/` directory should contain the unpacked, unmodified corpus data as found in the URLs listed in `SOURCE`. If there are more than one source URLs, there should be one subdirectory in `original-data/` for each. When appropriate, these subdirectories should be named consistently with other repositories, for example `train/` for training data, `devel/` for development/validation data, and `test/` for test data.

Whenever possible, the URLs in `SOURCE` should point to the actual corpus data packages so that their download can be automated.

**Example**: in the [`ncbi-disease`](http://github.com/openbiocorpora/ncbi-disease) repository, [`SOURCE`](http://github.com/openbiocorpora/ncbi-disease/blob/master/SOURCE) contains

```
http://www.ncbi.nlm.nih.gov/CBBresearch/Dogan/DISEASE/NCBItrainset_corpus.zip
http://www.ncbi.nlm.nih.gov/CBBresearch/Dogan/DISEASE/NCBIdevelopset_corpus.zip
http://www.ncbi.nlm.nih.gov/CBBresearch/Dogan/DISEASE/NCBItestset_corpus.zip
```

and [`original-data/`](http://github.com/openbiocorpora/ncbi-disease/tree/master/original-data) contains the subdirectories

```
train/
devel/
test/
```

## Corpus metadata

(TODO)
