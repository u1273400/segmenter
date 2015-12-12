

## Title  
SPPAS : a tool for the phonetic segmentation of speech

## Aims ##
Technical Overview of Sppas a tool to produce automatic corpora annotation including
- utterance
- syllabic
- phonemic
- word
annotation from prerecorded speech.
GUI interface makes the tool easy to use for various target audiences including computer scientists and linguists.

## Key Concepts ##
SEGMENTATION TOOL,

## Finding ##
- The biggest obstacles of linguists is not the storage of data nor its analysis but its annotation.
- Tools for analysis of speech include
 1. Anvil (Keep, 2001r)
 2. Elan (Sloetjes et al., 2010r)
 3. Praat (Boersma and weenik, 2009r)
 4. Transcriber (TranscriberAG, 2011r)
 5. WaveSurfer (WaveSurfer, 2012r)
- Tools for speech alignment
 1. HTK toolkit (Young & Young, 1994r)
 2. Sphinx (Carnegie Mellon University, 2011r)
 3. Julius (Nagoya Institute of Technology, 2010r)
- Key advantage of Sppas is the simplicity such that it can be used directly by linquist without the help of a software engineer.
- Sppas modules
 1. Inter Pausal Unit
 2. Phoneticizer
 3. Alignment
 4. Syllabification
- Sppas resources
 1. Phonetic dictionary
 2. Acoustic Model (AcM) trainer: Ideally, unique articulatory-acoustic correlates.  *But acoustic properties of a given phone can be affected by* intra- and inter- speaker variability as well as the environment and therefore the notion of *context dependent models such as* diphones and triphones are adopted.
- Sppas packages
 1. dict - pronounciation dictionaries
 2. models - acoustic hmm models
 3. syll - syllabification configuration
 4. samples - sample annotations
 5. lib - sppas routines
 6. tools - sppas tools modules
  1. wavsplit.py - performs IPU segmentation
  2. phonetize.py - uses a dictionary
  3. aligment.py - uses phonized output and hmm  model
  4. momel.py and Syll\*.jar to produce syllables and pitch targets.
  5. wavcut.py, wavestats.py, wav2intensity.py - additional tools

![](https://selene.hud.ac.uk/u1273400/images/seg_media/sppas.PNG)


### Inter Pausal Unit (IPU)
The IPU algorithm identifies silent pauses in the recorded speech signal and *attempts to align them with the* IPUs *proposed in the transcription, under the assumption that each such unit is separated by a silent pause. For a given minimum duration for pauses and for inter-pausal units a dichotomic search adjusts the silence threshold (in dB) and identifies the number of units thus defined. The search halts when the three parameters are correctly adjusted: minimal duration of pauses, minimal duration of units and silence threshold.

### Phoneticizer
Phonetization can be acheived by two means: *dictionary based solution* consisting of maximum phonetic knowledge lexicon and *rule based systems based on inference approaches or proposed by* linguist experts.  Both methods however require manual human input to complete correctly. SPPAS convention for phonetization is as follows 
- spaces separate tokens
- dots separate phonemes
- pipes separate phonetic variants.

For example the phrase 'je suis' is phonetized as follows:

 ʒ|ʒ.ɘ|ʃ s.ɥ.i.z|s.u.i|ɥ.i|ɥ.i.z

### Alignment
*To perform alignment, a finite state grammar that describes sentence patterns to be recognized and an acoustic model are needed.  A grammar essentially  defines constrains on what the SRE can expect as input.  It is a list of words that the SRE listens to.  Each word has a set of asociated list of phonemes, extracted from the dictionary.  When given a speech input, the SRE searches for the most likely word sequence under constraint of the given grammar*.  

### Syllabification
A rule-based system performs a phoneme-to-syllable segmentation based on 2 principles
1. *a syllable contains a vowel, and only one.
2. a pause is a syllable boundary*
*These two principles focus the problem of the task of find- ing a syllabic boundary between two vowels. As in state-of- the-art systems, phonemes were grouped into classes and rules established to deal with these classes*.

## Limitation ##
The statistical model includes HMMs that require training data.  Also, word segmentation is a little primitive. Sentence/clausal segmentation is not present

## Relation ##
Presents a robust toolkit that is accessible.  

## Comment ##
Recent developments in computational linguistics have given rise to large quantities of linguistic data being collected.  These corpus of information are not very easy to analyse and Bigi(2011) has rightnly observed that a fairly efficient method of analysis speech corpora requires phonetic alighment of the recording with a phonetic transcription of the speech.

According to Bigi(2011) *Speech alighment requires an acoustic model.* This model was implemented in SPPAS as a file having statistical representations of each phoneme in the phonetic alphabet of the language. A combination of the acoustic model along with segmented phonentized speech is able to accomplish speech alignment.  The production of the acoustic model themselves is however achieved using *Gaussian mixture densities whose parameters are estimated using an expectation maximization (EM) procedure.*  The accuracy of the training procedure depends on the volume of accurately annotated data.  Therefore the larger the size of the training data, the more accurate the model. The procedure is also enhanced by extracting the *Mel-frequency ceptrum coefficients (MFCC)* along with their standard derivatives.

SPPAS deals with new languages by adding the language resources to the following appropriate directories
1. Acoustic model
2. Dictionary
3. Syllabification rules

### Sppas Library modules
1. wav - contains three classes Wave, WavePitch and waveSil to deal with wav files.
2. trs - deals with a set of transcribed files in 'Tier' format. *A tier is a set of 'Annotation' instances.   Annotations are represented by a label and 1 or 2 time values, depending on the annotation type: interval or point*.
3. phon - Set of classes handling phonetization
4. align - For alignment
5. momel - set of classes modeling the analysis and synthesis of intonation patterns.*INTSINT is an acronym for INternational Transcription System for INTona- tion. INTSINT codes the intonation of an utterance by means of an alphabet of 8 discrete symbols constitut- ing a surface phonological representation of the into- nation: T (Top),H(Higher),U(Upstepped), S (Same), M(mid), D (Downstepped), L (Lower), B (Bottom)*.


## REFERENCE ##

Bigi, B. (2012). SPPAS : a tool for the phonetic segmentation of speech, 1748–1755.
