--------------------------------------------------------------------------------------------------
    XL-WiC: A Multilingual Benchmark for Evaluating Semantic Contextualization
--------------------------------------------------------------------------------------------------

This package contains the XL-WiC datasets for evaluating multilingual contextualized word representations. 

Datasets are organized per type:
- xlwic_wikt_monolingual/ contains train test and validation datasets extracted from Wiktionary for each language. Moreover, it contains two extra datasets used for analysis purposes: IV.test.txt and OOV.test.txt. IV indicates In-Vocabulary test sets. These contain only words that have been seen at training time. OOV indicates Out-Of-Vocabulary test sets. These contain only words that have not been seen at training time.
- xlwic_wikt_xlingual/ contains English train and validation datasets from the English WiC dataset, and test sets extracted from Wiktionary.
- xlwic_wn_xlingual/ contains English train and validation datasets from the English WiC dataset, and validation and test datasets extracted from WordNet for each language.

The files follow a tab-separated format:
target_word <tab> PoS <tab> start-index_1 <tab> end-index_1 <tab> start-index_2 <tab> end-index_2 <tab> example_1 <tab> example_2 <tab> label

- "target_word": the target word which is present in both examples.
- "PoS": the Part-of-Speech tag of the target word (either "N": noun or "V": verb).
- "start-index_i": indicates the start char index of target_word in "i"th example. 
- "end-index_i": indicates the end char index of target_word in "i"th example. 
- "example_i": corresponds to the "i"th example.
- "label": can be 1 or 0 depending on whether the intended sense of the target word is the same in both examples or not.


NOTE 1: The gold test labels are kept secret as it is being used as the basis for a public competition in CodaLab: https://competitions.codalab.org/competitions/27071


For further details, please see https://pilehvar.github.io/xlwic/


====================================================================================================
REFERENCE PAPER
====================================================================================================

When using this dataset, please refer to the following paper:

	Alessandro Raganato, Tommaso Pasini, Jose Camacho-Collados and Mohammad Taher Pilehvar,
	XL-WiC: A Multilingual Benchmark for Evaluating Semantic Contextualization,
	In Proceedings of EMNLP 2020.
