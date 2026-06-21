# Imagined speech EEG dataset — vowels condition (Nguyen et al. 2017)

## Overview

This dataset comprises preprocessed EEG recordings from 8 healthy subjects performing imagined speech tasks involving three vowel phonemes (a, i, u). Participants received auditory and visual cues to imagine speaking each vowel, with 64-channel EEG data acquired at 256 Hz. The dataset includes 7,200 trials (8 subjects × 300 trials × 3 overlapping 2-second epochs per trial) analyzed using Riemannian manifold-based feature extraction and relevance vector machine classification, achieving approximately 49% mean accuracy across a 10-fold cross-validation scheme.

## Dataset Summary

| Property | Value |
|---|---|
| Subjects | 8 |
| Channels | 64 |
| Classes | 3 |
| Trial length | 5 s |
| Sampling frequency | 256 Hz |
| Sessions | 1 |
| Total trials | 2400 |
| Paradigm | MotorImagery |

## Data Collection Methods

EEG data were acquired using a BrainProducts ActiCHamp system with 64 channels (60 EEG, 4 EOG) at 256 Hz sampling rate using a standard 10-20 montage. The experimental paradigm consisted of auditory beeps at 1.0 s intervals with visual cues, during which subjects imagined speaking designated vowels. Preprocessing included bandpass filtering (8-70 Hz, 5th order Butterworth), 60 Hz notch filtering, and adaptive EOG artifact removal. Feature extraction employed Riemannian tangent space mapping with common spatial pattern spatial filtering across mu (8-13 Hz), beta (13-30 Hz), and gamma (30-70 Hz) frequency bands.

## How to Access via MOABB

Install MOABB and load this dataset directly:

```python
from moabb.datasets import Nguyen2017_V
from moabb.paradigms import MotorImagery
paradigm = MotorImagery()

dataset = Nguyen2017_V()
X, y, metadata = paradigm.get_data(dataset)
```

For more details see the [MOABB documentation](https://moabb.neurotechx.com/) and the
[MOABB dataset page](https://moabb.neurotechx.com/docs/generated/moabb.datasets.Nguyen2017_V.html).

## Citation

If you use this dataset please cite the primary publication:

> DOI: [10.1088/1741-2552/aa8235](https://doi.org/10.1088/1741-2552/aa8235)

## NEMAR / MOABB Benchmark Collection

This BIDS-formatted dataset was converted from the original data using the
[MOABB](https://moabb.neurotechx.com/) pipeline and re-hosted on
[NEMAR](https://nemar.org/) as part of the MOABB benchmark collection.
The original data and license terms apply — see `dataset_description.json` for details.
