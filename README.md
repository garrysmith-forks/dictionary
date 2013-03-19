WordNet Dictionary
==================

The dictionary service provides a JSON API for looking up words in WordNet
and matching the against a particular corpus.

## Requirements

PostgreSQL 9.1+
Erlang R15B03

[See Zephyr Install Guide](https://github.com/airships/zephyr/wiki/Install)


## Setup

```bash
# initialize the database
make setup
# start the service
script/dictionary console
```

## Seed Wordnet

```bash
# from Erlang console
(tag_analysis@127.0.0.1)1> tag_analysis_import_wordnet:do("../dictionary-seed/wordnet/Thesaurus/Thesaurus_a-z.csv").
```

## Querying

```bash
curl -v http://localhost:10001/tags/software%20development
```
