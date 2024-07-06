This task is centered around the analysis of EEG data to classify different cognitive states
using advanced deep learning techniques.

[Dataset](https://physionet.org/content/eegmat/1.0.0/)

### Choice of Models:
1. **EEGNet** as it was specifically designed for EEG signal classification. It is lightweight, making it suitable for real-time applications and deployment on devices with limited computational power.
2. **TSCeption** as it can handle the temporal and spectral characteristics of EEG signals
3. **ATCNet** because it is designed to handle temporal dependencies in EEG data.

### PSD Inference:
The rest state shows a higher power across all frequencies than the task state.
These results seem to support notions I read that brain activity is better during rest/sleep. Be it retention, dreams, healing etc.
[more](https://colab.research.google.com/github/NNL-Keerthana/DeepLearning_EEG/blob/main/PSD_featureExtraction.ipynb#scrollTo=UDsVlFjGCTi9&line=5&uniqifier=1)

### Classification Results:
| *Model*    |*Accuracy*| *Precision*| *Recall* |*F1-Score*|
| -----------|:--------:|:----------:|:--------:| --------:|
| EEGNet     |  0.8000  | 0.7000     | 1.0000   |    0.8235|
| TSCeption  | 0.8000   |   0.8100   |  0.8000  |   0.8000 |
| ATCNet     |   0.4667 | 0.4667     | 1.0000   | 0.6364   |

While fine-tuning the hyperparameters and experimenting with the architecture, preference was given to Higher Recall.
Because we are dealing with EEG signals. In cases like medical diagnostics missing a positive case is critical.
