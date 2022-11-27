## Preamble
The following describes a fictitious corpus made to be situated in the universe of the podcast textit{Ars Paradoxica}. All of the persons, entities, and events introduced past this box are purely fictional.
		
With that said, this corpus was inspired by GRAEC (Kasselimis et al. 2020) and the [Fromkin Speech Error Database](httpswww.mpi.nldbmpisedbsperco_form4.pl). All of the data were obtained by hand-picking lines of dialogue from the transcripts on [arsparadoxica.com](httpsarsparadoxica.com).

# Butterfly Syndrome Speech Error Dataset (BSSED)
## Introduction
Butterfly Syndrome (BS) is one of the most common and most dangerous occupational hazards in the United States Office of Developed Anomalous Resources (ODAR). Its most identifiable symptom is tense-specific aphasia. We have compiled examples of the resultant speech errors into the Butterfly Syndrome Speech Error Dataset (BSSED) in the hopes that the data therein will be able to inform clinicians identify and researchers study BS.

## Data
In 1955, Morales and Sharma (1955) began broadcasting a series of audio recordings that had been disseminated from the Blackroom from its anchor point in 1943. Recall that BS is a common hazard at ODAR; since these recordings had all passed through ODAR's communications nexus, then, it should not be surprising that many of them include speech from individuals with BS. 

It is understood that the Blackroom has shared with the world every audio recording that had crossed its desk. Morales and Sharma (1955) have shared a small portion of this data, about 18 hours' worth of speech. We hope that these actors will publish more recordings in the future, but in the meantime, their existing broadcasts have been transcribed by the href{httpsarsparadoxica.com}{textit{Ars Paradoxica}} team.

The utterances used in this corpus were hand-selected from these transcripts. Given a list of individuals known to have BS, annotators located these individuals' utterances that displayed the disfluencies now known as signs of the disorder.

All of the data in this corpus are freely available. Anyone who listens to the broadcasts in question or reads their transcripts has access to the knowledge contained herein. That includes patients' names, severity of illness, treatment, and other sensitive details. Even so, information that can be used to identify subjects has been omitted.

## Annotation
Data has been collated into XML files, one per subject. In our pilot work, we identified three types of speech errors tense-aspect-mood (TAM), lexical, and omission. Each subject's file contains one section for each of these categories.

### Tense-Aspect-Mood
Erroneous utterances are listed by instance. These are then sorted by type, as described below. An instance is structured as follows

```
instance episode=06
  utteranceI will see... I've seen that, clear as day.
    precedentWhat you are making has limitless potential to change the world.precedent
  utterance
  actual explicit=true tense=future aspect=unmarked voice=active targetspan=0~9 aux=beI will seeactual
  correct explicit=true tense=present aspect=perfect voice=active targetspan=14~23 aux=haveI've seencorrect
instance
 ```
 
 ### Lexical and Omission
 
 ```
 instance episode=06
    utteranceBut only where you find the right answer.
        precedentWe've talked about this.precedent
    utterance
    actual explicit=true targetspan=9~13whereactual
    correct explicit=falsewhencorrect
 instance
```
 
```
instance episode=06
    utteranceNot acceptable.utterance
    actual targetspan=0 missing=S Vactual
    correctThat iscorrect
instance
```

## Findings
As of this dataset's most recent update, this dataset only contains examples from one patient. This patient, however, can demonstrate a good deal about BS's effect on speech. We have a good number of recordings of this subject spanning from their introduction to time travel in 1943, through the worsening of their symptoms up to 1946, and even some after very effective CAGE therapy nearly eliminated their condition. The disordered speech samples in this corpus were all uttered before this treatment.

This subject has exhibited more aphasic speech errors than many others with BS, and certainly more than the other subjects we have access to. We have access to 24 such instances. Unsurprisingly, this subject's TAM errors became more severe as their condition degraded. Toward the culmination of their symptoms, they would utter multiple incorrect auxiliaries multiple times before every verb.

We also found that most of this subject's lexical errors involved time-related words. Within one recording midway through the development of their condition, this subject made the following replacements:

| Uttered  | Correct  |
| -------  | -------  |
| span     | room     |
| thinking | thoughts |
| where    | when     |
| next to  | until    |

All of these except for textit{thinking}textit{thoughts} are clearly time-related. This is not surprising, and it reinforces our knowledge that the speech defects seen in BS are closely tied to the patient's perception of time.

Most intriguingly, we found that in most of this subject's TAM errors (10 of 17), the subject was textit{I} or textit{we}. We have yet to perform a full analysis of this subject's speech, but to the naked eye, it seems that most of their statements have other named entities as subjects. BS is caused by a break in one's perception of causality, particularly in relation to textit{oneself}. It makes sense, then, that a patient would have more difficulty with TAM when talking about oneself.

### Future work
Our next plan of action is to collate data like the above for other subjects in Morales and Sharma's broadcasts. 
We would also like to create a corpus of these patients' non-disordered speech, so that we can directly compare it with their BS-affected speech. This will be a larger undertaking, but not by much; we can still obtain this data rather simply from Morales and Sharma's broadcasts.

Given the small amount of data we have available, it is unlikely that this dataset will ever be large enough to train machine learning models. However, we believe it is worthwhile to compile this data nonetheless. Even at this elementary stage, we have observed multiple heretofore unnoticed patterns in our subject's speech. We hope that these observations, and ones gleaned later on in our research, will help clinicians identify, diagnose, and treat BS.