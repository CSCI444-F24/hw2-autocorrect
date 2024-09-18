### Overview
This repository contains (188k train + 23k val + 23k test) chat messages that have 0 or more typos in them (in `assignment_data`). Train and val also have the corrected message (target output i.e. 'gold' messages).

### Baselines
The `perfect` model predicts the correct (un-typo'ed) answer for the validation fold. The `ostrich` model does not change the input, and hopes that there are no typos to fix! These baseline "predictions" are in `val_predictions` and the itemized+aggregate performances are in `val_performances`.

### Evaluation
The `eval.py` file provides six measures of performance based on character and word matches. It takes separate arguments for gold messages, predicted messages, output directory, output prefix, and (optionally) `ostrich` summary performance (used for measuring relative performance).
