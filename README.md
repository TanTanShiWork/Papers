# TTS and VC Related Papers
## Content
1. [Speech Synthesis](#speech-synthesis)
    1. [General](#general)
    1. [Multi-speaker](#multi-speaker)
    1. [Multi-lingual](#multi-lingual)
    1. [Expressive](#expressive)
    1. [Voice clone](#voice-clone)
    1. [Singing](#singing)
    1. [Front-end](#front-end)
    1. [Vocoder](#vocoder)
2. [Voice Conversion](#voice-conversion)
___________________________________________________________________________________________________________________________

## [Speech Synthesis](#content)

### [General](#content)
___________________________________________________________________________________________________________________________

### [Multi-speaker](#content)
<details>
<summary> <b>Training Multi-Speaker Neural Text-to-Speech Systems Using Speaker-Imbalanced Speech Corpora.</b> in Interspeech, 2019 
    <a href="https://arxiv.org/pdf/1904.00771.pdf">pdf</a>
    <a href="https://nii-yamagishilab.github.io/sample-tts-speaker-imbalanced/">samples</a>
    </summary> 
    
   - Resampling techniques(Under-sampling of the majority speakers / over-sampling of the minority speakers) are applied in training. Related papers:<a href="https://sci2s.ugr.es/keel/pdf/algorithm/congreso/kubat97addressing.pdf">[1]</a>,<a href="https://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.35.1693&rep=rep1&type=pdf">[2]</a>,<a href="https://arxiv.org/pdf/1106.1813.pdf">[3]</a>
   - Model ensemble. Average-based combination functions are defined to combine the output(MGC & F0) of the 3 subsystems. Subsystems' architecture are same, but trained on different subsets of training corpus.
   - 10 female Japanese spk * 1k~10k utt/spk; spk: 10-dim one-hot vector; speaker-independent WaveNet vocoder trained using MGC and quantized mel-scale F0s
   - speaker dependent\ under sampled\ multi-speaker\ over sampled\ ensemble models are compared.
</details>

___________________________________________________________________________________________________________________________

### [Multi-lingual](#content)
___________________________________________________________________________________________________________________________

### [Expressive](#content)
___________________________________________________________________________________________________________________________

### [Voice clone](#content)
voice clone & speaker adaptation & zero/one/few-shot 
<details>
<summary> <b>AdaSpeech: Adaptive Text to Speech for Custom Voice.</b> in ICLR, 2021 
    <a href="https://arxiv.org/pdf/2103.00993.pdf">pdf</a>
    <a href="https://speechresearch.github.io/adaspeech/">samples</a>
    </summary> 
    
   - Two challenges: 1.different acoustic conditions between custom voice and source speech; 2. trade-off between fine-tuning parameters (memory storage) and voice quality.
   - Solution to challenge1: Modeling acoustic conditions in both utterance level and phoneme level. train: both extracting from target speech and add to the phoneme hidden sequence; inference: utt-from reference speech, phoneme-from acoustic predictor(build upon phoneme encoder)
   - Solution to challenge2: Conditional layer normalization:using speaker embedding as the conditional information to generate the scale and bias vector in layer normalization. In fine-tuning, only adapt the parameters related to the conditional layer normalization(including speaker embedding). The number of CIN = decoder layer * 2 + 1.
   - Backbone: FastSpeech2. Speaker representation: speaker ID (embedding)-256dim. Vocoder: MelGAN
   - Source model: LibriTTS(2456 speakers-586h), 16kHz. 20 sentences and 2k steps for adaptation.
   - GT \ baseline(spk) \ baseline(dec) \ Adaspeech are compared.
</details>

- **Sample Efficient Adaptive Text-to-Speech.** in ICLR, 2019.
[pdf](https://arxiv.org/pdf/1809.10460.pdf)
[samples](https://sample-efficient-adaptive-tts.github.io/demo)

- **Transfer Learning from Speaker Verification to Multispeaker Text-To-Speech Synthesis,** in NeurIPS, 2018.
[pdf](https://arxiv.org/pdf/1806.04558.pdf)
[samples](https://google.github.io/tacotron/publications/speaker_adaptation)

- **Fitting New Speakers Based on a Short Untranscribed Sample,** in ICML, 2018.
[pdf](http://proceedings.mlr.press/v80/nachmani18a/nachmani18a.pdf)
[samples](https://ytaigman.github.io/fitspk/index.html)

- **Neural Voice Cloning with a Few Samples,** in NeurIPS, 2018.
[pdf](https://arxiv.org/pdf/1802.06006.pdf)
[samples](https://audiodemos.github.io)
___________________________________________________________________________________________________________________________
### [Singing](#content)
<details>
<summary> <b>Semi-supervised Learning for Singing Synthesis Timbre,</b> arXiv, 2020 
    <a href="https://arxiv.org/pdf/2011.02809.pdf">pdf</a>
    <a href="https://mtg.github.io/singing-synthesis-demos/semisupervised/">samples</a>
    </summary> 
    
   - .
  ![image](https://user-images.githubusercontent.com/1402048/87929772-3e218000-ca87-11ea-9f13-9869bee96b57.png)
</details>

___________________________________________________________________________________________________________________________
### [Front-end](#content)
___________________________________________________________________________________________________________________________
### [Vocoder](#content)
___________________________________________________________________________________________________________________________
## [Voice Conversion](#content)
