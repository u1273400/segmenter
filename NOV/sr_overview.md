
## Speech Recognition Overview

### Introduction

*We can classfify speech recognition tasks and systems along a set of dimensions that produce various tradeoffs in applicability and robustness.*

#### Isolated word versus contiuous speech

*Some speech systems only need identify single words at a time (e.g., speaking a number to route a phone call to a company to the appropriate person), while others must recognise sequences of words at a time.  The isolated word systems, are not surprisingly, easier to construct and can be quite robust as they have a complete set of patterns for the possible inputs.  Continuous word systems cannot have complete representation s of all possible inputs, but must assemble patterns of smaller speech events (e.g., words) into larger sequences (e.g. sentences)*

#### Speaker Dependent versus speaker independent systems

*A speaker dependent system is a system where the speech patterns are constructed (or adapted) to a single speaker.  Speaker independent systems must handle a wide range of speakers.  Speaker dependent systems are more accurate, but the training is not feasible in many applications.  For instance, an automated telephone or operator system must handle any person that calls in, and cannot ask the person to go through a training phase before using the system.  With a dictation system on your personal computer, on the other hand, it is feasible to ak the user to perform a hour or so of training in order to build a recognition model.*

#### Small versus vocabulary systems
*Small vocabulary systems are typically less than 100 words (e.g. speech interface for long distance dialing), and it is possible to get quite accurate recognition for a wide range of users.  Large vocabulary systems e.g. say 20,000 words or greater), typically need to be speaker dependent to get good accuracy (at least for systems that recognise in real time).  Finally, there are mid-size systems, on the order of 1000-3000 words, which are typical sizes for current research-based spoken dialog systems.*

*Some applications can make restrictive assumption possible.  For instance, voice dialing on cell phones has a small vocabulary (less than 100 names), is speaker dependent (the user says every word that needs to be recognized a couple of times to train it), and isolated word.  On the other extreme, there are research systems that attempt to trascribe recordings of meetings among several people.  These must handle speaker independent, continuous speech, with large vocabularies.  At present, the best research systems cannot achieeve must better than a 50% recognition rate, even with fairly high quality recordings. *

### Speech Recognition as a tagging problem
*
Speech recognition can be viewed as a generalization of the tagging problem:  Given an acoustic ouptut $A_{1,T}$ (consisting of a sequence of acoustic events $a_1,\dots,a_T$) we want to find a sequence of words $_{1,R}$ that maximimizes the probability.*

*Using the standard reformulation for tagging by rewriting  this by Bayes Rule and then dropping the denominator since it doesn't affect the maximisation, we transform the problem into computing.*

$$argmax_wP(A_{1,T}|W_{1,R}){1,R})$$
*
In the speech recognition work, $P(W_{1,R})$ is called the **language model** as before and $P(A_{1,T}|W_{1,R})$ is called the **acoustic model**.*

*This formulation so far, however, seems to raise more questions that answers.  In particular, we will address the main issues briefly here and then return to look at them in detail in the following sections.
*

### What does a speech signal look like?
*
Human speech can best be explored by looking at the intensity at different frequencies over time.  This can be shown graphically in a spectogram of signal containing one word such as shown in Figure 1 below.
*
![Figure 1](https://selene.hud.ac.uk/u1273400/images/seg_media/spectogram.PNG)
**Figure 1:** Spectogram of the word "sad"

*Time is one the x-axis, frequency is on the y-axis, and the darkness of the area corresponds to intensity.  This word starts out with a log of high frequency noise with no noticiable lower frequencies of resonance (typical of an /s/ or /sh/ sound) startng at time 1.55, then at 1.7 there is a period of silence.  This iniital signal is indicative of a "stop" consonant such as a /t/, /d/, /p/.  Betwen 1.8 and 1.9 we see a typical vowel, with strong lower frequencies and distinctive bars of resonance called the **formants** clearly visible.  After 1.9 it looks like another stop consonant, that includes an area with lower freqeuncy and resonance.
*

### The sounds of Language
*
The sounds of language are classified into what are called **phonemes**.  A phoneme is a minimal unit of sound that has semantic content e.g. the phoneme AE versus the phoneme EH captures the difference between the words "bat" and "bet".  Not all acoustic changes change meaning.  For instance, singing words at different notes doesn't change meaning in english.  Thus changes in pitch does not lead to phenemic distinctions.
*

*Often we talk of specific features by which the phonemes can be distinguished.  One of the most important features distinguishing  phonemes is **voicing**.  A voiced phoneme is one that involves sound from the vocal cords.  For instance, F (e.g. "fat") and V (e.g. "van") differ primarily in the fact that in the latter, the vocal chords are producing sound, i.e. it is voiced, whereas, the former does not i.e. unvoiced.  Here's a quick breakdon of the major classes of phonemes.
*

#### Vowels
*
Vowels are always voiced, and the differences in English depend mostly on the formants (prominent resonances) that are produced by different positions of the tongue and lips.  Vowels generally stay steady  over the time they are produced by different positions of the tongue and lips.  Vowels generally stay steady over the time they are produced.  By holding the tongue to the front and varying its height we get vowels IY (beat), IH (bit), EH (bat), and AE (bet).  ith tongue in the mid position, we get AA (bob - bahb), ER (bird), AH (but), and AO (bought), With the tongue in the back position we get UW (boot), UH (book), and OW (boat).  There is another class of vowels called **diphthongs**, which do change during their duration.  They can be thought of as starting with one vowel and ending with another. For example AY (buy) can be approximated by starting with AY (bob) and ending with IY (beat). Similarly, we have AW (down, cf. AA W), EY (bait, cf. EH IY), and OY (boy, cf. AO, IY).
*

#### Consonants
*
Consonants fall into general classes, with many having voiced and unvoiced members*
##### 1. Stops or Plosives
*These all involve stopping the speech stream (using lips, tongue, etc.) and then rapidly releasing a stream of sound.  They come in voiced, unvoiced pairs. P and B, T and D, and K and G.*
##### 2. Fricatives
*These all involve "hissing" sounds generated by constraining the speech streem by the lips, teeth etc.  They also come in unvoiced and voiced pairs. F and V, TH and DH (e.g. thing versus that), S and Z, and finally SH and ZH (shut vs azure).*
##### 3. Nasals
*These are all voiced and involve moving air through the nasal cavities by blocking it with the lips, gums, and so on.  We have M, N and NX (sing).*
##### 4. Affricatives
*These are like stops followed by *


