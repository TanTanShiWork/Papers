# TTS and VC Related Papers
## Content
1. [Speech Synthesis](#speech-synthesis)
    1. [General](#general)
    1. [Front-end](#front-end)
    1. [Vocoder](#vocoder)
    1. [Multi-lingual](#multi-lingual)
    1. [Expressive](#expressive)
    1. [Voice clone](#voice-clone)
    1. [Singing](#singing)
2. [Voice Conversion](#voice-conversion)

## [Speech Synthesis](#content)

### [General](#content)

### [Front-end](#content)

### [Vocoder](#content)

### [Multi-lingual](#content)

### [Expressive](#content)

### [Voice clone](#content)
voice clone & speaker adaptation & zero/one/few-shot 
1. **Sample Efficient Adaptive Text-to-Speech.** in ICLR, 2019.
[pdf](https://arxiv.org/pdf/1809.10460.pdf)
[demo](https://sample-efficient-adaptive-tts.github.io/demo)

1. **Transfer Learning from Speaker Verification to Multispeaker Text-To-Speech Synthesis,** in NeurIPS, 2018.
[pdf](https://arxiv.org/pdf/1806.04558.pdf)
[demo](https://google.github.io/tacotron/publications/speaker_adaptation)

1. **Fitting New Speakers Based on a Short Untranscribed Sample,** in ICML, 2018.
[pdf](http://proceedings.mlr.press/v80/nachmani18a/nachmani18a.pdf)
[demo](https://ytaigman.github.io/fitspk/index.html)

1. **Neural Voice Cloning with a Few Samples,** in NeurIPS, 2018.
[pdf](https://arxiv.org/pdf/1802.06006.pdf)
[demo](https://audiodemos.github.io)

### [Singing](#content)
1. **Semi-supervised Learning for Singing Synthesis Timbre,** arXiv, 2020
[pdf](https://arxiv.org/pdf/2011.02809.pdf)
[demo](https://mtg.github.io/singing-synthesis-demos/semisupervised/)

<details>
<summary> <b>Semi-supervised Learning for Singing Synthesis Timbre,</b> arXiv, 2020 
    <a href="https://arxiv.org/pdf/2011.02809.pdf">pdf</a>
    <a href="https://mtg.github.io/singing-synthesis-demos/semisupervised/">demo</a>
    </summary> 
    
   - A derivation of Deep Voice 3 model using non-causal convolutional layers.
   - Teacher-Student paradigm to train annon-autoregressive student with multiple attention blocks from an autoregressive teacher model.
   - The teacher is used to generate text-to-spectrogram alignments to be used by the student model.
   - The model is trained with two loss functions for attention alignment and spectrogram generation.
   - Multi attention blocks refine the attention alignment layer by layer.
   - The student uses dot-product attention with query, key and value vectors. The query is only positinal encoding vectors. The key and the value are the encoder outputs.
   - Proposed model is heavily tied to the positional encoding which also relies on different constant values.
  ![image](https://user-images.githubusercontent.com/1402048/87929772-3e218000-ca87-11ea-9f13-9869bee96b57.png)
</details>


## [Voice Conversion](#content)
