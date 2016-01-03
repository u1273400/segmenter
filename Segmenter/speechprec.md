
## Speech Characteristics

*Despite many differences between individuals, and existence of many languages, speech folows general patternas, and on average has well defined characteristics such as those of volume, frequency distribution, pitch rate and syllabic rate.*(McLoughlin, 2009) 

### Speech Classification
*Physically, sounds of speech can be described in terms of a pitch countour and format frequencies.  In fact this description forms a method of analysis used by most speech compression algorithms.  Formants are resonant frequencies of the vocal tract which appear in the speech spectrum as clear peaks.  As an example, three distinct formant speaks can bee seen inthe frequency domain plot of a short speech recording shown in figure 1 below.*
![Figure 1: Formants](https://selene.hud.ac.uk/u1273400/images/seg_media/formants.PNG)
**Figure 1:** Spectrum plot of a 20ms recording of speech, showing three distinct peaks (McLoughlin, 2009).

*Formants have been described by the famous research Klatt and others as single most important feature in speech communications.  Generally many formants will be present in a typical utterance, and the location of these will vary over time a the shape of the mouth changes.  Formants are counted from the lowest frequency upwards, and usually only the first three (F1, F2 and F3) contribute significantly to the intelligibility of speech.  Some fricative sounds like /ch/ can produce lots of formants but generally speaking F1 contains most of the speeche energy while F2 and F3 contribute more to speech intelligibility*.

*The pitch contour (often called f0 - note the lower case notation) is the parameter that describes the tone of the voice (the perceived frequency) and it is in effect the fondamental vocal frequency.  Again, pitch frequencies contain energy but contribute little to intelligibility for English and European langauges.  It is however, a very different matter in a tonal language such as Mandarin Chinese which is totally dependent on tone for conveying meaning.  As an example, in Chinese the single word 'ma' can mean one of five things depending on which tone it is spoken with: mother, horse, scold, question, etc.*

### Amplitude distribution of speech
*The overall amplitude distribution of speech depends on the speaker's personality and mood (every reader is likely to have endured monotonous talks on occasion - literally meaning 'single tone' speech), environmental noise, infection and so on.*

*Also, feedback from a listener, either verbal 'speak up please' or non-verbal such as cupping hand around an ear can prompt a speaker to alter their vocal characteristics.  However, despite this variability, itis interesting to determine average speech levels in different environments.*

*In general, as the noise level increases by 1 dB, a speaker will raise his voice level by 0.5 dB within the range of normal speech.  With very low noise levels, a male adult speaker can produce 52 dB<sub>SPL</sub> of speech measured at a distance of 1m when speaking casually.  This raises to about 90 dB<sub>SPL</sub> when shouting.  The dynamic range of conversational speech is around 30 dB<sub>SPL</sub>, and the mean level for males measured at 1m is somewhere in the region of 55-60 dBA<sub>SPL</sub> ('A' refers to the perceptual correction A-weighting curve)*

## Speech Understanding
*There are non-auditory factors involved in the understanding of speech by humans.  That is, the nature of speech structure and how that relates to understsanding, rather than the nature of human hearing and perception of speech which is a topic of psychoacoustic analysis.*

### Intelligibility and Quality
Intelligibility and Quality can be used interchangeably at times, but their measurement and dependencies are actually quite different.  *In very simple terms, quality is the measure of the fidelity of the speech.  This includes how well the speech under examination resembles some original speech, but extends beyond that how nice the speech sounds.  It is highly subjective measure but can be approximated objectively.*

### Measurement of Speech Intelligibility


### Measurement of Speech Quality


## Analysis Toolkit

### Zero-crossing rate ZCR
It is a simple algorithm to determine the pitch that works well in the absence of noise.  It is designed to be a simple computational means to count how many times the speech signal crosses the zero axis for a window time period.  *The number of crossings per second will equal twice the frequency.  If we define sign { } to be a function returning +1 or 0 depending on whether the signal is greater than zero or not, then the ZCR for the ith analysis frame, of length N can be determined as*

### Frame Power
*This is the meaure of the signal energy over an analysis frame.  For speech frame i, with N elements, denoted by $x_i()$, the frame power meaure is determined from *
$$ E_i=\frac{1}{N}\sum_{n=0}^{N-1}{|x_i(n)|^2}  - - - - \dots(2) $$

    function [fpow]=fpow(segment)
        fpow=sum(segment.ˆ2)/length(segment);

### Average magnitude difference function

*The average magnitude difference function is designed to provide much of the information of the frame powermeasure, but without multiplications*

## Speech Analysis and classification

*The analysis of speech is an important requirement of many different applications and the classification of speech into various categories is a necessary part of many techniques.  The folloing ives basic techniques of applications of speech analysis and classification*

1. detecting the presence of speech (VAD).
2. detecting voiced and unvoiced speech
3. finding boundaries between phonemes or words
4. classifying speech by phoneme type
5. language detection
6. speaker recognition
7. speech recognition.

*Classification is an important, and growing area of speech research which relates to the machine 'understanding' of speech (where understanding can range from knowing whether a speech is present right through to understanding the meaning or emotion conveyed by the spoken text.)*

*In order to begin such classification of speech, it is usually necessary to first perform some form of meaurement on the speech signal itself.  For example detecting voiced or unvoiced speech might require the determination of speech power and pitch, perhaps through examination of LSP data.  Many methods can potentially be used for analysis of speech, and extensive empirical testing is almost always required to determine the subset of meaures to be used for a particular application.*

### Pitch Analysis

### Joint time-frequency Distribution (JTFD)

## Speech Recognition Preprocessing Analysis

*The main requirement for speech recogntion is the extraction of voice features, which may distinguish different phonemes of a language.  From a statistical point of view, this procedure is equivalent to finding a sofficient statistic to estimate phonemes*(Becchetti & Ricotti, 1998).  This has to be independent of the following other speech characteristics including
1. phonatory apparatus
2. speaker mood
3. age
4. sex
5. dialect inflections and
6. noise

*To decrease vocal message ambiguity,* speech is therefore prefiltered before recognition. *Filtering is performed on discrete time quantised speech signals. Hence the first procedure consists of an analog to digital conversion.  Then the extraction procedure of the significant* speech features.  Cepstral analysis is used to demonstrate feature extraction methods.

### Physical Features of speech signals
*
The frequency bandwidth of a speech signal is about 16kHz.  However, most of the speech energy is under 7kHz.  Speech bandwidth is generally reduced in recording.  A speech signal is called orthophonic if all the spectral components over 16kHz are discarded.  A telephonic lower quality signal is obtained whenever a signal does not have energy out of the band 300-3400Hz.  Therefore, digital speech processing is usually performed by frequency sampling ranging between 8 kHz and 32 kHz. These give a bandwidth of 4 kHz and 16 kHz respectively.
*

*
Voice is produced by the phonatory mechanism articulators.  These are in a stable position for a very short time during the production of a phoneme, and then they move to a different stable position through an articulatory transition movement.  This is why a speech signal has a relevant variation each 80-200ms. 
*

*
 A simple but effective mathematical model of the physiological voice production process is the excitation and vocal tract model.  The excitation represents the sound produced by the part of the phonatory physical system including the lungs and vocal cords, while the vocal tract is the duct through which the air passes to the mouth.  The excitation requires  a different mathematical description in the case of voiced or unvoiced sounds.
*

*
The excitation  signal is assumed periodic with a period equal to the pitch for vowels and other voiced sounds, while for unvoiced consonants, the excitation is assumed to be white noise, i.e. a random signal without dominant frequencies.  The excitation signal is subject to spectral modifications while it passes through the vocal tract that has an acoustic effect equivalent to linear time invariant filtering.  These modifications contribute to the final sound characteristic features of different phonemes of a language.
*

*
The model is significant because for each type of excitation, a phoneme is identified mainly by considering the shape of the vocal tract.  Therefore, the vocal tract configuration can be estimated by identify the filtering performed by the vocal tract on the excitation.  Introducing the power spectrum of the signal $P_x(\omega)$, we have:
*
$$ P_x(\omega)=P_v(\omega)P_h(\omega) - - - - \dots (1) $$
*
Where $\omega$ is the frequency of the discrete time signal.  
*

### Signal Processing
*
The characteristics of the vocal tract define the current uttered phoneme.  Such characteristics are evidenced in the frequency domain by the location of the formants i.e. the peaks given by resonances of the vocal tract.  Althrough possessing relevant information, high frequency formants have smaller amplitude with respect to low frequency formants.  A preemphasis of high frequencies is therefore required to obtain similar amplitude for all formants.  Such processing is usually obtained by filtering the speech signal with a first order  FIR filter whose transfer function is in the z-domain is:
*
$$ \begin{aligned} H(z) =  1- a.z^{-1} & & \text{for } 0\le a \le 1 - - - - \dots (2) \end{aligned} $$

*a being the preemphasis parameter.  In essence, in the time domain, the preemphasized signal is related to the input signal by the relation:*
$$ x'(n)=x(n)-ax(n-1) $$
*
A typical value for a is 0.95, which gives rise to a more than 20 dB amplification of the high frequency spectrum.  Further pre-processing such as noise cancelling can be performed.  Finally, HMM-based ASR may experience a significant reduction in performance if temporally long silences are not removed from speech.  Since these silences should not be processed by ASR, effective speech detectors are required.  Simple detectors based on energy may be sufficient when the signal to noise ratio does not change appreciably.  
*

### Windowing

*Traditional methods for spectral evaluation are reliable in the case of a stationary signal (i.e. a signal whose statistical characteristics are invariant with respect to time).  For voice, this holds only within the short time intervals of articulatory stability, during which a short time analysis can be performed by "windowing" a signal x'(n) into a succession of windowed sequences x<sub>t</sub>(n), t=1,2,...,T, called frames, which are then individually processed.


### Spectral Analysis

## References

Becchetti, C., & Ricotti, L. P. (1998). Speech recognition: theory and C++ implementation. New York: Wiley. 

McLoughlin, I. (2009). Applied speech and audio processing: With Matlab examples. Cambridge: Cambridge University Press.



```R

```
