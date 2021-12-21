
PLEWI - polish errors correction challenge
==========================================

Correct polish grammatical errors.

Your main goal is to correct errors in texts, using machine translation methods.

Format of train set
-------------------

The train set has just two columns separated by TABs:
* Sentence with error.
* Corresponding corrected sentence.

Train set is compressed with xz tool, in order to uncompress it, run:
```
xzcat train/train.tsv.xz > train/train.tsv
```

Format of train and dev sets
-------------------

Train and dev sets consist of two .tsv files (without TABs):
* in.tsv - sentences with errors.
* expected.tsv - corrected sentences.


Evaluation metrics
-------------------

One evaluation metric is used:
* BLEU


Directory structure
-------------------

* `README.md` — this file
* `config.txt` — configuration file
* `train/` — directory with training data
* `train/train.tsv.xz` — compressed sample parallel corpus (Text with errors in the first column, corrected text in the second one)
* `dev-0/` — directory with dev (test) data
* `dev-0/in.tsv` — Input text (sentences with errors) for the dev set
* `dev-0/expected.tsv` — Corrected sentences for the dev set
* `test-A` — directory with test data
* `test-A/in.tsv` — Input text (sentences with errors) for the test set
* `test-A/expected.tsv` — Corrected sentences for the test set
