
## Speech Synthesis (Holmes & Holmes, 2001)
- Message synthesis from stored waveforms is a long-established technique for providing a limited range of spoken information.  The simplest systems join together word-size units.  The technical quality of the speech can be high, but it is not possible to produce good results for a wide range of message types
- Synthesis from diphones gives complete flexibility of message content, but is limited by the difficulty of making the diphones represent all the articulation effects that occur in different phonetic environments.  To obtain the best quality from diphone synthesis, care must be taken in selecting and excising the examples.  Quality may be improved by adding to the simple diphone set to include allophone-based units or longer units spanning several phones.
- Vocoders rquire a small fraction of the memory needed for simple waveform storage, and also make it easy to vary the pitch and timing, and to smooth the joins between any units being concatenated.  Synthesis quality is, however, limited by the inherent vocoder quality.
- The technique known as pitch-synchronous overlap-add (PSOLA) allows good synthesis quality to be achieved by concatenating short waveform segments.  Smooth joins are obtained by concatenating segments pitch-synchronously and overlapping the end of one segment with the start of the next.
- By decomposing the speech signal into pitch periods with overlapping windows, prosodic modifications are easy with PSOLA.  Timing can be modified by repeating or removing individual pitch periods, and pitch can be changed by altering the spacing between windows before resynthesis.
- Time-domain PSOLA is simple to implement, but needs a lot of memory and cannot smooth any spectral discontinuities occuring at segement boundaries.
- Other variants of PSOLA address the above limitations by incorporating some parametric representation of the speech, such as LPC or MBE coding, while retaining the PSOLA technique for prosodic modifications.
- The hardware cost for synthesis from stored human speech is dominated by the memory requirements except for multi-channel systems.

### Synthesis by Rule
- Phonetic sysnthesis by rule involves applying acoustic-phonetic rules to generate synthesizer control parameters from a description of an utteracnce in terms of a sequence of phonetic segments together with prosodic information.
- Most acoustic-phonetic rule systems are designed for a formant synthesizer.
- A convenient implementation is to store the rules as tables of numbers for use by a single computational procedure
- Typically, a table for each phone holds some target synthesizer control values, together with transition durations and information used to calculate the controls at the nominal boundary between any pair of phones.  Such a system can capture musch of the coarticulation effects between phones.
- Separate tables can be included for any allophone variation which is not captured by the coarticulation rules.  The total number of different units will still be far fewer than the number required in a concatenative system.
- Acoustic-phonetic rule systems have tended to be set up 'by-hand', but automatic procedures can be used to derive the paraemeters of these systems, based on optimizing the match of the synthesized speech to phonetically transcribed natural speech data.


### Template Matching speech recognition
- Most early successful speech recognition systems worked by pattern matching on whole words.  Acoustic analysis, for example by a bank of band-pass filters, describes the speech as sequence of feature vectors, which can be compared with stored templates for all the words in the vocabulary using a suitable distance metric.  Matching is improved if speech level is coded logarithmically and level variations are normalised.
- Two major problems in isolated-word recognition are end-point detection and timescale variation.  The timescale problem can be overcome by dynamic programming (DP) to find the best way to align the time scales of the incoming word and each template (known as dynamic time warping).  Performance is improved by using penalties for timescale distortion.  Score pruning, which abandons alignment paths that are scoring badly, can save a lot of computation.  
- DP can be extended to deal with sequences of conneceted words, which has the added advantage of solving the end-point detection problem.  DP can also operate coninuously, outputting words a second or two after they have been spoken.  A wildcard template can be provided to cope with extraneous noises and words that are not in the vocabulary.
- A syntax is often provided to prevail illegal sequences of words from being recognized.  This method increases accuracy and reduces the computation.

### Large vocabulary speech recognition
- Some large-vocabulary recognition tasks may require accurate transcription of the words that have been said, while others will need understanding of semantic content (but not necessarily accurate recognition of every word).
- For speech transcription the task is to find the most likely sequence of words, where the probability for any one sequence is given by the product of the acoustic-model and language model probabilities.
- The principles of continuous speech recognition using HMMs can be applied to large vocabularies, but with special techniques to deal with the large number of different words that need to be recognized.
- It is not practical or useful to train a separate model for every word, and instead sub-word models are used.  Typically phone-size units are chosen, with pronunciation of each word being provided by a dictionary.
- Triphone models represent each phone in the context of its left and right neighbours.  The large number of possible triphones is such that many will not occur in any given set of training data.  Probabilities for these triphones can be estimated by 'backing off' interpolating with biphones (dependent on only the left or the right context) or even context-independent monophones.
- Another option, which allows greater context specificity to be achieved, is to group ('cluster') similar triphones together and share ('tie') their parameters.  A phonetic decision tree can be used to find the best way to cluster the triphones based on questions about phonetic context.  The idea is to optimize the fit to the data while also having sufficient data available to train each tied state.
- An embedded training procedure is used, typically starting by estimating parameters for very general monophone models for which a lot of data are available.  These models are used to initialize triphone models.  The triphones are trained and similar states are then tied together.  Multiple-component mixture distributions are introduced at the final stage.
- The purpose of the language model is to incorporate langauage constraints, expressed as probabilities for different word sequences.  The perplexity, or average branching factor, provides a meaure of how good the language modelis at predicting the next word given the words that have been so far.
- N-grams model the probability of a word depending on just the immedately N-1 words, where typically N=2 ('bigrams') or N=3 ('trigrams'). 
- The large number of different possible words is such that data sparsity is a massive problem for language modelling, and special techniques are needed to estimate probabilities for N-grams that do not occur in the training data.
- Probabilities for N-grams that occur in the training text can be estimated from frequency counts, but some probability must be 'freed' and made available for those N-grams that do not occur.  Probabilities for these unseen N-grams can then be estimated by backing off or interpolating with more general models.
- The principles of HMM recognition extend to large vocabularies, with a multiple-level structure in which phones are represented as networks of states, words as networks of phones, and sentences as networks of words.  In practice the decoding task is not straightforward due to the very large size of the search space, especially if cross-word triphones are used.  Special treatment is also required for langauge models whose probabilities depend on more than the immediately preceeding word (i.e. for models more complex than bigrams).  The one-pass Viterbi search can be extended to operate with cross-word triphones and with trigram language models, but the search space becomes very large and is usually organized as a tree.  Efficient pruning is essential.
- An alternative search strategy uses multiple passes.  The first pass identifies a restricted set of possibilities, which are typically organized as an N-best list, a word lattice or a word graph.  Later passes select between thee possibilities.  Another option is to use a depth-first search.
- Automatic speech understanding needs further processing of the speech recogniser output to analyse the meaning, which may involve syntactic and semantic analysis.  To reduce the impact of recogntion errors, it is usual to start with an N-best list or word lattice.  Partial parsing techniques can be used for syntactic analysis to deal with the fact that the spoken input may be impossible to parse completely because parts do not fit the grammar, due to grammitacal errors, hesitations and so on.
- Meaning is often represented using templates, which will be specific to the application and have 'slots' that are filled by means of a linguistic analaysis.
- In a spoken dialogue systems, a dialogue manager is used to control the interaction with the user and ensure that all necessary information is obtained.
- ARPA has been influential in promoting progress in large vocabulary recognition and understanding, by sponsoring the collection of large databases and running series of competitive evaluations.  Error rates of less than 10% have been achieved for transcribing unlimited-vocabulary read speech and for understanding spoken didalogue queries.  Recognition of more casually spoken spontaneous speech is still problematic.



```python

```

## References

Holmes, J. N., & Holmes, W. (2001). Speech synthesis and recognition (2nd ed.). New York: Taylor & Francis.
