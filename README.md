# Coptic Scriptorium - Corpora

This is the public repository for Coptic SCRIPTORIUM corpora.  The documents are available in multiple formats: CoNLL-U, relANNIS, PAULA XML, TEI XML, and TreeTagger SGML (`*.tt`). The `*.tt` files generally contain the most complete representations of document annotations, though note that corpus level metadata is only included in the PAULA XML and relANNIS versions.

Corpora can be searched, viewed, and queried with complex queries http://data.copticscriptorium.org.  Project homepage is http://copticscriptorium.org

## Metadata and annotation quality

Metadata about each document is most easy to obtain by looking at the first line of files in the respective `*_TT` directory of each corpus. Five types of annotation quality metadata are available:

  * segmentation (Coptic internal word splitting or bound groups and morphemes)
  * tagging (parts of speech, using the Scriptorium fine-grained tagset)
  * parsing (Universal Dependencies parses)
  * entities (classification of all referring expressions into 10 categories)
  * identities (linking of all named entity spans to corresponding Wikipedia articles, a.k.a. Wikification)

Values for these metadata are:

  * automatic - machine annotations only 
  * checked - checked for accuracy by an expert in Coptic
  * gold - closely reviewed for accuracy, usually as a result of treebanking

## Notes on duplicates and redundancies

Some of the data in this repository contains **duplicate information**. In particular, the `coptic-treebank` corpus is a convenient collection of all gold-standard treebanked data (manual syntactic analyses), all of which is included in other source corpora (which are often not 100% gold parsed). The documents in the treebank are **identical** to the same documents in the source corpora (e.g. XH204-216 is included in both its source corpus folder `shenoute-fox` and the treebank).

Additionally, individual book corpora from the Old and New Testaments with some or all manual annotations (`sahidica.mark`, `sahidica.1corinthians`, `sahidic.ruth`) are also represented in the large and completely automatically annotated `sahidica.nt` and `sahidic.ot`. Versions of documents from these sources may differ slightly in the analyses in these corpora, and the individual book corpora are generally more accurate.

Finally, some documents represent parallel witnesses of other documents (different manuscript versions of the same conceptual text). These are not necessarily text-identical to each other, but quantitative work in which double-counting the same or very similar text is undesirable may wish to filter these out. They can be identified in `*.tt` files by the metadatum `redundant="yes"`.

## Sources and licenses 

All the documents are licensed CC-BY 3.0 (https://creativecommons.org/licenses/by/3.0/us/) or 4.0 (https://creativecommons.org/licenses/by/4.0/) unless otherwise indicated.  Major exceptions include:

-  Sahidica New Testament specific license (http://www.copticscriptorium.org/download/corpora/Mark/coptic_nt_sahidic.html)

-  Canons of Apa Johannes CC-BY-SA 3.0 (https://creativecommons.org/licenses/by-sa/3.0/)

-  Sahidic Old Testament CC-BY-SA 4.0 (https://creativecommons.org/licenses/by-sa/4.0/)

Individual files also contain licensing information.
