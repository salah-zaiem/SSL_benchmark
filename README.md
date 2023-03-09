# The-audio-benchmark

This repository contains the code used to generate the results presented in the paper entitled : "Speech Self-Supervised Representation Benchmarking:Are We Doing it Right?". The paper reports the results of several experiments that were conducted using specific datasets. The code contained in this repository was used to preprocess the data, train the models, and generate tables that are presented in the paper. The code relevant to our work is contained in the folder "speechbrain-develop/SSL\_benchmark/"
We tried to remove any name in the SSL files, but if you happen to find an author list in one of the training files, be aware it is not linked to the authors of the paper as it is the name of the authors of the original SpeechBrain recipes we started from.


# Data
Links to all datasets used in our experiments :

- [LibriSpeech ASR](https://www.openslr.org/12) : Download the train-clean-100 and both test-clean and test-other and dev-clean

- [SLURP](https://zenodo.org/record/4274930)

- [Other languages](https://commonvoice.mozilla.org/en/datasets) : Choose Common Voice Corpus 11.0 and download Basque and Welsh

- [IEMOCAP](https://sail.usc.edu/iemocap/)

- [Buckeye](https://buckeyecorpus.osu.edu/)

- [VoxCeleb](https://mm.kaist.ac.kr/datasets/voxceleb/)


# Use 
Let's take the example of SLURP. To run a downstream evaluation, go to the folder "speechbrain-develop/SSL\_benchmark/SLURP/direct/linear/" and run 
```
python weighted_train.py hparams/ssl_encoder_large.yml --output_folder <your_output_folder> --hub <model_huggingface_hub>
```
after changing the data paths in the Yaml file.

All the folders are organised as follows : Task/DownstreamArchitecture/


# License

* Free software: MIT


