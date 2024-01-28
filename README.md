# HMS---Harmful-Brain-Activity-Classification

[associated competition](https://www.kaggle.com/competitions/hms-harmful-brain-activity-classification/overview)

[associated paper](https://www.acns.org/UserFiles/file/ACNSStandardizedCriticalCareEEGTerminology_rev2021.pdf)

**Goal**: Detect AND Classify types of harmful brain activity.

There are six patterns of interest for this competition: seizure (SZ), generalized periodic discharges (GPD), lateralized periodic discharges (LPD), lateralized rhythmic delta activity (LRDA), generalized rhythmic delta activity (GRDA), or “other”. 

**How brain activity is recorded?**

![download](https://github.com/JeanJulesBigeard/HMS---Harmful-Brain-Activity-Classification/assets/48935007/2f0d34ba-48f5-46b2-9ab6-72e72047b04f)

Electroencephalography, commonly referred to as EEG, is a non-invasive method used to record electrical activity in the brain. This technique involves placing electrodes on the scalp, which detect tiny electrical charges that result from the activity of brain cells. The signals captured by these electrodes are amplified and recorded, typically resulting in a series of wavy lines that are analyzed by specialists.

![download](https://github.com/JeanJulesBigeard/HMS---Harmful-Brain-Activity-Classification/assets/48935007/85ec420f-1687-42d8-a937-91fa48710e01)

**How electroencephalography data looks like?**

Electroencephalography (EEG) data typically appears as a series of wavy lines, each representing the electrical activity recorded from different electrodes placed on the scalp. These lines, called traces, show the voltage changes over time. The patterns observed in EEG data are influenced by the brain activity of the individual, and they can vary significantly depending on the state of consciousness, activity, or any neurological conditions.

**What are we looking for in these data?**

We are looking for patterns such as:

**Wave Patterns**: EEG data is characterized by different types of wave patterns, such as alpha, beta, delta, and theta waves. Each type corresponds to different brain states. For example, alpha waves are often associated with a state of relaxation, while beta waves are linked with active thinking or concentration.

**Amplitude and Frequency**: The waves have varying amplitudes (heights) and frequencies (speeds). The amplitude indicates the strength of the signal, and frequency shows how fast the brain waves are oscillating.

**Artifacts**: These are non-brain waveforms that can appear in the data due to muscle movements, eye blinks, or electrical interference.

**Abnormal Patterns**: In cases of neurological disorders like epilepsy, the EEG may show spikes, sharp waves, or other unusual patterns that indicate abnormal brain activity.


**How spectrograms related to EEG?**

![download](https://github.com/JeanJulesBigeard/HMS---Harmful-Brain-Activity-Classification/assets/48935007/39879a18-d365-4e3b-900a-155920330328)

Spectrograms are closely related to EEG in the context of analyzing and visualizing the frequency spectrum of brain waves over time. A spectrogram is a visual representation of the spectrum of frequencies of a signal as they vary with time. In the case of EEG data, a spectrogram can provide valuable insights into the frequency content of the brain's electrical activity.

**How spectrograms are used in relation to EEG?**

**Frequency Analysis**: EEG signals consist of brain waves with different frequencies, like alpha, beta, theta, and delta waves. A spectrogram can visually display these frequencies, showing how they change over time during the EEG recording.

**Identifying Patterns**: Spectrograms can help in identifying patterns that might not be easily discernible in the raw EEG waveforms. For example, they can be used to detect changes in brain activity during different sleep stages, or to identify oscillatory activity associated with certain neurological disorders, like epilepsy.

**Temporal and Frequency Resolution**: A key advantage of spectrograms in EEG analysis is their ability to provide information about both the timing (temporal resolution) and the frequency (frequency resolution) of brain waves. This is crucial for understanding dynamic changes in brain activity.

**Data Visualization**: Spectrograms offer a more intuitive way to visualize and interpret complex EEG data. They can transform the EEG's time-domain data into a more accessible frequency-domain representation, which can be easier to analyze and understand, especially in research and clinical diagnostics.

**What is LPD/GPD/LRDA/GRDA conditions and how they may be seen in data?**

<img width="620" alt="download" src="https://github.com/JeanJulesBigeard/HMS---Harmful-Brain-Activity-Classification/assets/48935007/ff7a2574-a637-474f-a356-7c69ba9acc65">

**1-/ Lateralized Periodic Discharges (LPDs)** are typically associated with acute or subacute brain dysfunction, often related to structural brain lesions or acute brain injuries. LPDs are of particular interest in the field of neurology and are often investigated in patients with acute neurological symptoms such as seizures or altered mental status.

**Lateralization**: LPDs are lateralized, meaning they predominantly occur on one side (hemisphere) of the brain.

**Periodicity**: LPDs are periodic, meaning they display a repeating pattern. This periodicity is a key feature in their identification on an EEG.

**Waveform Characteristics**: LPDs typically consist of sharp waveforms or complexes that are clearly distinguishable from the background EEG activity. These sharp waves are usually followed by a slow-wave component.

**General Characteristics**: In EEG data, LPDs appear as regular, sharply contoured waveforms that stand out against the background brain activity and repeat at consistent intervals. They are usually unilateral, affecting either the left or right hemisphere, which is an important aspect in their interpretation.


**2-/ Generalized Periodic Discharges (GPDs)** are EEG patterns often associated with diffuse or generalized brain dysfunction. These discharges can be linked to various neurological conditions, ranging from toxic-metabolic encephalopathies to severe diffuse brain injuries. GPDs are of significant interest in clinical neurophysiology and neurology, particularly in the context of diagnosing and managing patients with altered consciousness or comatose states.

**Generalized Distribution**: GPDs are characterized by their distribution across both hemispheres of the brain, rather than being localized to one side.

**Periodicity**: Like LPDs, GPDs exhibit a repeating pattern. Their periodic nature is crucial for their identification on EEG and distinguishes them from other generalized EEG abnormalities.

**Waveform Characteristics**: GPDs usually consist of repetitive, sharply contoured waveforms that can vary in shape and duration. They are often more synchronized compared to other EEG patterns.

**Clinical Implications**: GPDs may be seen in various clinical scenarios, including severe diffuse brain injury, hypoxic-ischemic encephalopathy, and in association with certain drug toxicities or metabolic derangements. Their presence can indicate a severe underlying brain dysfunction.

**3-/ Lateralized Rhythmic Delta Activity (LRDA)** refers to a particular EEG pattern characterized by rhythmic, slow-wave activity, typically in the delta frequency range, and is usually localized to one hemisphere.

**Lateralization**: The key feature of LRDA is its lateralized nature, affecting predominantly one hemisphere of the brain, which can be crucial in localizing a neurological lesion or dysfunction.

**Rhythmic Delta Waves**: Unlike the sharp waveforms of LPDs, LRDA is defined by smoother, more rhythmic waveforms, predominantly in the delta frequency range (1-4 Hz).

**Clinical Context**: LRDA is often observed in patients with focal brain lesions, such as those caused by stroke, tumors, or inflammation. It may also be seen in the context of focal seizure activity.

**Interpretation**: The presence of LRDA in an EEG reading can provide valuable information regarding the location and possibly the nature of brain pathology, aiding in diagnosis and treatment planning.

**4-/ Generalized Rhythmic Delta Activity (GRDA)** is an EEG pattern characterized by rhythmic delta activity that is distributed more uniformly across both hemispheres of the brain.

Generalized Distribution: GRDA differs from LRDA in that it is not lateralized but involves both hemispheres, often symmetrically.

Rhythmic Delta Waves: This pattern is defined by continuous or quasi-continuous rhythmic delta waves. The activity is slower and more rhythmic compared to GPDs.

Associated Conditions: GRDA can be seen in various clinical conditions, including encephalopathies of different etiologies (like toxic-metabolic disturbances), and in some cases, during certain sleep stages or in diffuse brain disorders.

Diagnostic Significance: The presence of GRDA can be indicative of a global brain dysfunction and may warrant further investigation to identify its cause. It is particularly significant in assessing patients with altered levels of consciousness or diffuse neurological impairments.
