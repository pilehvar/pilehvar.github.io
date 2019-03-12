--------------------------------------------------------------------------------------------------
	WiC: 10,000 Example Pairs for Evaluating Context-Sensitive Representations
--------------------------------------------------------------------------------------------------

This package contains the WiC dataset for evaluating contextualized word representations. 

The dataset is split into development (dev), training (train) and test (test) sets. Each partition 
contains two files, with the same number of lines (each line corresponds to an instance):

    * (dev/train/test).data.txt: This is a tab-separated file containing the following items: 

        target_word <tab> PoS <tab> index1-index2 <tab> example_1 <tab> example_2

	    - "target_word": the target word which is present in both examples.

   	    - "PoS": the Part-of-Speech tag of the target word (either "N": noun or "V": verb).

       	    - "index1-index2": indicates the index of target_word in example_1 and example_2, 
	       respectively.

            - "example_i": corresponds to the "i"th example. In this version all examples are 
			       tokenized.


    * (dev/train/test).gold.txt: This file contain the gold labels, which can be "T" (True) or 
	                         "F" (False) depending on whether the intended sense of the 
				 target word is the same in both examples or not.


For further details, please see https://pilehvar.github.io/wic/

NOTE: the test data is kept for the evaluation of a public competition (details to be announced on 
      the website). Meanwhile, you might use the development set for your evaluations.
