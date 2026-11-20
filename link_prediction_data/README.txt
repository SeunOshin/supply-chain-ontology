Link prediction data (step 7, part 3 of Project UAT.ipynb)

examples.csv              The real links and the false links made from them, in three sets:
                          random pairs (as in the paper), wrong part and wrong buyer, wrong part.
                          Made with a fixed seed, so every run gives the same file.
embeddings.npz            Each sentence and company name as 384 numbers from the pretrained
                          language model all-MiniLM-L6-v2 (sentence-transformers). Saved so the
                          notebook runs without loading the model. A text that is not in this
                          file is worked out when first needed and added.
measures.csv              Balanced accuracy, precision, recall and F1 for each method on each set
                          of false links, five-fold, tested on suppliers not seen in training.
<case>_predictions.csv    For each kind of part a case uses, the five best-scoring suppliers seen
                          shipping that part that the BOM does not record.

The real links come from importyeti_data/link_table.csv. Nothing here is typed in by hand.
