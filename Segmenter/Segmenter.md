



## Abstract
Concatenative speech synthesis requires a speech database comprising of speech units. For a particular language a unique speech database will comprise all the various speech units of the language and will vary for different languages. Two crucial tasks for the formation of speech databases will be to determine the phonetic alphabet for the target language and the ability to phonetically transcribe speech from the target language into a formal orthographic system.

This paper examines the different methods for preparing concatenative speech synthesis speech databases and proposes automatic means for determining the phonetic alphabet speech units as a reverse engineering method of automatically transcribing speech from a target language. In this paper French and Okrika were used as the target languages.


## <span style="color:00ff00">Introduction</span>
TTS by concatenative model requires speech segments to be concatenated to form audible speech in a text-to-speech implementation.  In order to achieve this, speech segments are created from pre-existing recordings.  The creation of this segment database is usually strenuous, time consuming and manual (Bigi, 2012; Goldman, 2011).


### Aims

The aim of this report will be to discover novel ways to automatically segment speech and discover the necessary segments or phonemes using DSP, NLP and machine learning methods.


### Objectives
- Generation of diphone/triphone-based segments
- determination of unique di-phones and tri-phones
- determination of phonemes
- measure of correctness of phoneme determination
- measure of closeness of diphones and phonemes
- alternative means of diphone/triphone/phoneme classification.

### Methods
- test driven and integration approach
- cross-correlation
- speech acoustic analysis
- analysis of speech segmentation tools
- comparison of speech dsp methods
- analysis/comparison of machine learning techniques


## Literature

### Java Speech API (JSAPI)

The Java Speech API comprises speech engines. A speech engine can either be a synthesiser or a recogniser.

#### relevance to the grand scheme of things

The final speech segmenter and recogniser application will be implemented based upon the java speech API and as such, JSAPI tool forms as a background to the grand scheme of the overall implementation. 


#### Java speech markup language

This comprises production elements, structural elements and other miscellaneous elements


### z-Transform

The z-transform is a constrained version of the Discrete Time Fourier
Transform(DTFT). If we compare the DTFT to the z-transform, equations (1) and
(2) below

$$
X(z)= \sum \limits_{n=\infty }^{\infty}{x[n]z^{-n}} 
$$

[@equation1]

$$
X(z)= \sum_{n=-\infty }^{\infty}x[n]e^{-j\omega n} 
$$

[@equation2]

We find essentially that the z transform is the DTFT constrained to
$z=e^{j\omega n}$.

It can be shown that the z-operator is a linear operator and that the weighted
time-shifted timed function is transferable between the signal and it’s
transform, that is:

$$
\sum_{n=-\infty }^{\infty}kx[n]e^{-j\omega n}=k \sum_{n=-\infty }^{\infty}x[n]e^{-j\omega n} 
$$

#### Region of Convergence

We also define a property of the z-transform called the Region of Convergence
which is the values of z for which there exists a z-transform.


## References

Bigi, Brigitte. "SPPAS: a tool for the phonetic segmentations of Speech." The eighth international conference on Language Resources and Evaluation. 2012.

Goldman, Jean-Philippe. "EasyAlign: an automatic phonetic alignment tool under Praat." (2011).

