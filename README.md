# A project for preprocessing files in the Corpus Gesproken Nederlands (CGN)
This project was originally made to import the CGN for usage in [DeepSpeech](https://github.com/mozilla/DeepSpeech), but has since been extended to also do some additional processing on this data. This code has been written for usage in my bachelor thesis: [Building A Speech-to-Text Engine for Dutch](https://ai.vub.ac.be/files/Ropke_Bachelor_thesis_1819.pdf).

## import_cgn.py
This script will create the training, validation and test splits neccessary for the DeepSpeech project. These splits will contain the path to the audio file, the size of this file and its transcription.

## split_cgn.py
This script generates smaller audio segments out of the original audio files in the dataset. These audio files have a minimum bound that was decided by testing with count_files.py.

## count_files.py
This file will calculate the amount of files that will be generated by split_cgn.py when using a certain minimum duration for the newly generated audio files.

## clean_data.py
This script takes a CSV generated by import_cgn.py and replaces/removes certain characters. This is done so that the resulting file can be used on the same alphabet as the alphabet used by the English models provided by DeepSpeech.
