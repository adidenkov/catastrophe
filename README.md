# [Catastrophe.tech](https://catastrophe.tech)
### Disaster Detection with Natural Language Processing.

Submission for HackViolet 2022.

## Features

- [x] NLP model for predicting disasters (**82.9%** accuracy).
  - [x] Inference on arbitrary text
- [ ] API endpoint for deploying the model
- [x] Front-end for presenting inference results
  - [x] Quality-of-life: custom domain, SSL certificate
  - [ ] Other visualizations: statistics, map
- [ ] Real-time inference on Twitter data
  - [ ] Firebase integration for data storage

## Project layout

* `dp_bert.ipynb` - pipeline for training the NLP model
  * Saves to a file called `model.h5` (not included due to size)
* `catastrophe.WordPress.xml` - export of the WordPress front-end
* `modelserve.yaml` & `app.yaml` - configuration files for the API endpoint
  * `main.py` & `client.py` - deploy and serve the model

## Setup

For detailed instructions on setting up the API, see `SETUP.md` (`README.md` of the reference code).

To re-deploy after updating files, call:
```bash
gcloud app deploy
```

## Sources

1. [Kaggle dataset of labeled Tweets](https://www.kaggle.com/c/nlp-getting-started/overview) and a [corresponding BERT solution](https://www.kaggle.com/gunesevitan/nlp-with-disaster-tweets-eda-cleaning-and-bert).
1. [GCP tutorial](https://github.com/GoogleCloudPlatform/ml-on-gcp/tree/master/tutorials/sklearn/gae_serve#requirements) on loading and deploying a pickled model.
1. Various Google Cloud tutorials.