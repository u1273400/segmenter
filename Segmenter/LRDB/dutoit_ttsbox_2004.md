

## Title  
TTSBOX: a MATLAB toolbox for teaching text-to-speech synthesis

## Aims ##
Hands on Exposure to TTS using MATLAB.  

## Key Concepts ##
SEGMENTATION TOOL, SEGMENTATION ALGORITHMS, TTS, 

## Finding ##
- Consists of the folloing modules
 1. preprocessor using fsm
 2. morphological analyser using lexicon
 3. bigram pos-tagger
 4. phrase determiner using chinks and chunks
 5. phonetization using cart
 6. target sequence units and unit selection
 7. unit concatenator.

- Steps for TTS process involve
 1. Morpho-syntactic analysis
  a. preprocessing
  b. morphological analysis
  c. contextual analysis
  d. syntactic-prosodic grouping
 2. Phonetization using decision trees
 3. Prosody Generation
 4. Catenative Synthesis


### Preprocessing


### Morphological Analysis

### Contextual Analysis

### Syntactic prosodic grouping

### Ponetization using decision trees

### Prosody Generation

### Catenative Synthesis


## Limitation ##


## Relation ##


## Comment ##

List of m-files and variables include
1. strtok
2. tts_preprocess_using_fsm
3. corpus_to_lexicons
4. genglish_morphflex
5. corpus_to_lexicons
6. lexicon_search
7. tts_morph_using_lexicons
8. lattice_get_all_paths
9. tts_tag_using_bigrams
10. genglish_test_bigrams
11. genglish_load_chinksnchunks
12. tts_phrase_using_chinksnchunks
13. genglish_test_chinksnchunks
14. cart_run
15. tts_phonetize_using_cart
16. genglish_test_cart
17. corpus_to_speech_corpus
18. tts_set_targets
19. tts_select_units
20. tts_concatenate_using_xcorr


## REFERENCE ##
Dutoit, T., & Cernak, M. (2005). TTSBOX: a MATLAB toolbox for teaching text-to-speech synthesis . Proceedings. (ICASSP ’05). IEEE International Conference on Acoustics, Speech, and Signal Processing, 2005 . IEEE . http://doi.org/10.1109/ICASSP.2005.1416359 

