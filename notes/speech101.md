---
title: "Speech 101: Introduction to speech processing"
layout: post
date: 2025-01-01
author: Herman Kamper
exclude: true
---

This is a self-paced course. The goal is to get you to modern speech recognition
and synthesis as quickly as possible. As a concrete aim, I want to get you to a
point where you can read the HuBERT paper ([Hsu et al.
2021](https://arxiv.org/abs/2106.07447)) and understand how speech recognition
is performed on top of HuBERT with the CTC loss ([Jurafsky and Martin 2025, Sec.
16.4](https://web.stanford.edu/~jurafsky/slp3/16.pdf)). Speech models are
typically combined with a text-based language model ([Jurafsky and Martin 2025,
Sec. 16.3](https://web.stanford.edu/~jurafsky/slp3/16.pdf)). So along the way
another aim would be that you have enough background to read some of the GPT
paper ([Radford et al.
2018](https://cdn.openai.com/research-covers/language-unsupervised/language_understanding_paper.pdf)),
which introduces arguably the most important language modelling approach of our
time.

The strategy for this course will be to go almost from scratch. It is completely
okay if you do not understanding everything immediately: there is quite a lot
and it normally takes time for things to sink in.

For most of my own videos, you can find links to the slides or accompanying
notes in the video comments.

Please let me know if you find any errors or typos in this document.



# Basic signal processing and speech science

- [Introduction to speech features](https://www.youtube.com/playlist?list=PLmZlBIcArwhN8nFJ8VL1jLM2Qe7YCcmAb)

    These videos describe feature extraction were an audio waveform is converted
    to a sequence of higher-level acoustic vectors. It is worth noting that,
    although you will still find such acoustic features in practice, many
    end-to-end speech models these days take in raw speech samples directly.
    I.e. if the audio signal is sampled at $16$ kHZ, then the input sequence
    $x_{1:T}$ to the speech model would consist of $16\,000$ floating values for
    every second of audio input.

- [Dynamic time warping](https://www.youtube.com/playlist?list=PLmZlBIcArwhMJoGk5zpiRlkaHUqy5dLzL)

    This is an old-school technique that is rarely used to do speech recognition
    directly these days. But it pops up quite often in low- and zero-resource
    speech applications.

- Speech 101 by Roger Moore [[slides](https://staffwww.dcs.shef.ac.uk/people/R.K.Moore/IS2020-Tutorial/RKM_IS2020-Tutorial_Speech-101.pdf)]:

    - [Part 1: Sound, speaking, hearing](https://staffwww.dcs.shef.ac.uk/people/R.K.Moore/IS2020-Tutorial/RKM_IS2020-Tutorial_Speech-101_part1.mp4) (48 min)
    - [Part 2: Sounds and symbols, articulatory phonetics, acoustic phonetics](https://staffwww.dcs.shef.ac.uk/people/R.K.Moore/IS2020-Tutorial/RKM_IS2020-Tutorial_Speech-101_part2.mp4) (44 min)
    - [Part 3: Phonology, prosody, behaviour](https://staffwww.dcs.shef.ac.uk/people/R.K.Moore/IS2020-Tutorial/RKM_IS2020-Tutorial_Speech-101_part3.mp4) (1 h)



# Machine learning

You need to get to a point where you understand neural networks, including
architectures like recurrent neural networks (RNNs), convolutional neural
networks (CNNs) and transformers. If you watch/read the following in the given
order, then you should be there:

- [Introduction to machine learning](https://www.youtube.com/playlist?list=PLmZlBIcArwhM_7t4ZzxXAs1PWaLqcPusG)

- Linear regression:

    - [Simple linear regression](https://youtu.be/L5-lxSGO9bM&list=PLmZlBIcArwhNd_sWiz6f1-NHc3lg3k7PF) (14 min)
    - [Vector and matrix derivatives](https://youtu.be/FCWrduAxf-Q&list=PLmZlBIcArwhNd_sWiz6f1-NHc3lg3k7PF) (13 min)
    - [Multiple linear regression - Model and loss](https://youtu.be/zu34zcyAFzU&list=PLmZlBIcArwhNd_sWiz6f1-NHc3lg3k7PF) (16 min)
    - [Polynomial regression and basis functions](https://youtu.be/TSFMepJbHa0&list=PLmZlBIcArwhNd_sWiz6f1-NHc3lg3k7PF) (15 min)
    - [Overfitting](https://youtu.be/S7B3LQJrU0w&list=PLmZlBIcArwhNd_sWiz6f1-NHc3lg3k7PF) (10 min)
    - [Regularisation](https://youtu.be/Zojp8z8GD8c&list=PLmZlBIcArwhNd_sWiz6f1-NHc3lg3k7PF) (15 min)
    - [Evaluation and interpretation](https://youtu.be/4hkZiGk66J8&list=PLmZlBIcArwhNd_sWiz6f1-NHc3lg3k7PF) (11 min)

- [Training, validating and testing](https://youtu.be/aXRDdjK-hI4) (18 min)

- [Maximum likelihood estimation](https://youtu.be/i6Rp0eiINgM&list=PLmZlBIcArwhPnCzcSUU5mF90aU_dMSnZ2) (20 min)

- Classification:

    - [Task](https://youtu.be/RqNaY7gnMP8&list=PLmZlBIcArwhMiJk7vCghuHGOGXXjC4n6b) (9 min)
    - [K-nearest neighbours](https://youtu.be/73YHJwp71hk&list=PLmZlBIcArwhMiJk7vCghuHGOGXXjC4n6b) (15 min)

- Logistic regression:

    - [Model and loss](https://youtu.be/nS6YewQAK7I&list=PLmZlBIcArwhOr0ysO1Hg4Wfoww0dZnHz4) (14 min)
    - [Gradient descent - Fundamentals](https://youtu.be/BlnLoqn3ZBo&list=PLmZlBIcArwhOr0ysO1Hg4Wfoww0dZnHz4) (11 min)
    - [Optimisation](https://youtu.be/SLhx32b7I3A&list=PLmZlBIcArwhOr0ysO1Hg4Wfoww0dZnHz4) (7 min)
    - [Basis functions and regularisation](https://youtu.be/D_rIX0xaYno&list=PLmZlBIcArwhOr0ysO1Hg4Wfoww0dZnHz4) (6 min)
    - [Multiclass - One-vs-rest classification](https://youtu.be/EYXSve6T5BU&list=PLmZlBIcArwhOr0ysO1Hg4Wfoww0dZnHz4) (5 min)
    - [Multiclass - Softmax regression](https://youtu.be/hYBwBmojXoU&list=PLmZlBIcArwhOr0ysO1Hg4Wfoww0dZnHz4) (15 min)

- [Preprocessing](https://www.youtube.com/playlist?list=PLmZlBIcArwhNSvaKyVSoIEq0ewNX9KTC4)

- [Introduction to unsupervised learning](https://youtu.be/_Tf1Vi4s7Ec&list=PLmZlBIcArwhMfNuMBg4XR-YQ0QIqdHCrl) (19 min)

- K-means clustering:

    - [Algorithm](https://youtu.be/PgK1IppRdsE&list=PLmZlBIcArwhMfNuMBg4XR-YQ0QIqdHCrl) (16 min)
    - [Details](https://youtu.be/f3-G0txYUEM&list=PLmZlBIcArwhMfNuMBg4XR-YQ0QIqdHCrl) (14 min)

- Introduction to neural networks:

    - [Neural network preliminaries: Vector and matrix derivatives](https://youtu.be/xOx2SS6TXHQ&list=PLmZlBIcArwhMHnIrNu70mlvZOwe6MqWYn) (5 min)
    - [Neural network preliminaries: The chain rule for vector derivatives](https://youtu.be/mnjSBg3EWZ0&list=PLmZlBIcArwhMHnIrNu70mlvZOwe6MqWYn) (7 min)
    - [Neural network preliminaries: Gradient descent](https://youtu.be/Ay3JdygFfY8&list=PLmZlBIcArwhMHnIrNu70mlvZOwe6MqWYn) (4 min)
    - [Neural network preliminaries: Logistic regression, softmax regression and basis functions](https://youtu.be/6QyxMO4wH2w&list=PLmZlBIcArwhMHnIrNu70mlvZOwe6MqWYn) (6 min)
    - [From logistic regression with basis functions to neural networks](https://youtu.be/_FWFutvALwo&list=PLmZlBIcArwhMHnIrNu70mlvZOwe6MqWYn) (19 min)
    - [Why is it called a neural network?](https://youtu.be/_QynHmmVn3E&list=PLmZlBIcArwhMHnIrNu70mlvZOwe6MqWYn) (4 min)
    - [Backpropagation (without forks)](https://youtu.be/6SW1oUztmzg&list=PLmZlBIcArwhMHnIrNu70mlvZOwe6MqWYn) (31 min)
    - [Backprop for a multilayer feedforward neural network](https://youtu.be/dTupaVdrz1k&list=PLmZlBIcArwhMHnIrNu70mlvZOwe6MqWYn) (4 min)
    - [Computational graphs and automatic differentiation for neural networks](https://youtu.be/fBSm5ElvJEg&list=PLmZlBIcArwhMHnIrNu70mlvZOwe6MqWYn) (7 min)
    - [What is the difference between negative log likelihood and cross entropy? (in neural networks)](https://youtu.be/ziq967YrSsc&list=PLmZlBIcArwhMHnIrNu70mlvZOwe6MqWYn) (9 min)
    - [Neural networks in practice](https://youtu.be/MvN0uD_A-mg&list=PLmZlBIcArwhMHnIrNu70mlvZOwe6MqWYn) (7 min)

- Before moving on to the videos below, it might actually be good to first cover
  the content in the [language modelling](#language-modelling) section below and
  then come back here and continue.

- Recurrent neural networks:
    
    - [D2L Sec. 9.4](https://d2l.ai/chapter_recurrent-neural-networks/rnn.html)
    - [From feedforward to recurrent neural networks](https://youtu.be/XImxbT8U0h8?list=PLmZlBIcArwhOSBWBgRR70xip-NnbOwSji) (15 min)
    - [RNN language model loss function](https://youtu.be/kUjXExou3Uw?list=PLmZlBIcArwhOSBWBgRR70xip-NnbOwSji) (9 min)
    - [RNN definition and computational graph](https://youtu.be/Q2UpMrpKI_M?list=PLmZlBIcArwhOSBWBgRR70xip-NnbOwSji) (3 min)
    - [Vanishing and exploding gradients in RNNs](https://youtu.be/VqYu8INY8co?list=PLmZlBIcArwhOSBWBgRR70xip-NnbOwSji) (13 min)
    - [Solutions to exploding and vanishing gradients (in RNNs)](https://youtu.be/xgMx_YBMU8c?list=PLmZlBIcArwhOSBWBgRR70xip-NnbOwSji) (10 min)
    - [Extensions of RNNs](https://youtu.be/iGkIIIgPFHQ?list=PLmZlBIcArwhOSBWBgRR70xip-NnbOwSji) (8 min)

- Convolutional neural networks:

    - [D2L Sec. 7.2](https://d2l.ai/chapter_convolutional-neural-networks/conv-layer.html)
    - [VGG convolutional neural network practical](https://www.robots.ox.ac.uk/~vgg/practicals/cnn/index.html)

        You only have to look at Part 1. This is part of the documentation for
        MatConvNet package (which I do not use), but I found this tutorial very
        helpful for getting a handle on convolutional neural networks.

        Most end-to-end speech recognition models use RNNs or transformer layers
        before the final classification layer, but often the early layers of the
        speech recognition system would be convolutional.

- Encoder-decoder models, machine translation and attention:

    - [A basic encoder-decoder model for machine translation](https://youtu.be/gHk2IWivt_8&list=PLmZlBIcArwhPHmHzyM_cZJQ8_v5paQJTV) (13 min)
    - [Training and loss for encoder-decoder models](https://youtu.be/aBZUTuT1Izs&list=PLmZlBIcArwhPHmHzyM_cZJQ8_v5paQJTV) (10 min)
    - [Encoder-decoder models in general](https://youtu.be/N8AzPeAORKM&list=PLmZlBIcArwhPHmHzyM_cZJQ8_v5paQJTV) (18 min)
    - [Greedy decoding](https://youtu.be/DW5C3eqAFQM&list=PLmZlBIcArwhPHmHzyM_cZJQ8_v5paQJTV) (5 min)
    - [Beam search](https://youtu.be/uG3xoYNo3HM&list=PLmZlBIcArwhPHmHzyM_cZJQ8_v5paQJTV) (18 min)
    - [Basic attention](https://youtu.be/BSSoEtv5jvQ&list=PLmZlBIcArwhPHmHzyM_cZJQ8_v5paQJTV) (22 min)

- [Self-attention and transformers](https://www.youtube.com/playlist?list=PLmZlBIcArwhOPR2s-FIR7WoqNaBML233s)



# Language modelling

Natural language processing (NLP) typically refers to text processing (rather
than speech processing). But speech recognition systems output text. So many NLP
techniques are also relevant in speech recognition systems. Most notably,
text-based language models (trained only on text) are often integrated into a
speech recognition system. The content below introduces the basics of NLP so
that you are able to understand state-of-the-art text-based language models.

- [What is natural language processing?](https://youtu.be/ZxG1YFrYuOU&list=PLmZlBIcArwhOqEQwyk2TBHmtEKTGPMu5d)

- [A first NLP example](https://youtu.be/k4Co_47zeO4&list=PLmZlBIcArwhOqEQwyk2TBHmtEKTGPMu5d)

- [Text normalisation and tokenisation](https://youtu.be/Y2FBKCwww50&list=PLmZlBIcArwhOqEQwyk2TBHmtEKTGPMu5d)

- [Byte-pair encoding (BPE)](https://youtu.be/20xtCxAAkFw&list=PLmZlBIcArwhOqEQwyk2TBHmtEKTGPMu5d)

- [Edit distance](https://youtu.be/C2cRO9BqlZw&list=PLmZlBIcArwhOqEQwyk2TBHmtEKTGPMu5d)

    To evaluate speech recognition systems, the output from the model is often
    compared to the transcription produced by a human. Normally the number of
    words in the two sequences don't match up exactly, so the edit distance
    algorithm is used to produce an alignment between the predicted and ground
    truth sequences. This alignment is then used to calculate a word error rate
    (WER); see the next section for more details on this metric.

- Language modelling with N-grams:

    - [The language modelling problem](https://youtu.be/6TjmCP7TDOg&list=PLmZlBIcArwhP-ril7Xe5vDNpdMEgOjppP)
    - [N-gram language models](https://youtu.be/SLsLEYZJ2xU&list=PLmZlBIcArwhP-ril7Xe5vDNpdMEgOjppP)
    - [Why use log in language models?](https://youtu.be/l5RgDfA2R-w&list=PLmZlBIcArwhP-ril7Xe5vDNpdMEgOjppP)

- [Neural networks examples: Natural language processing](https://youtu.be/dGo1BB5Wusk&list=PLmZlBIcArwhMHnIrNu70mlvZOwe6MqWYn)



# Large language models

- [Intro to large language models](https://youtu.be/zjkBMFhNj_g?si=dU7KNFP0_C_AQGuH) by Andrej Karpathy (1 h)
- [Large language model training and inference](https://youtu.be/Y9YmVNLslvs?list=PLmZlBIcArwhOVLRdimL3lS9F_33fzh9jU) (14 min)
- [The difference between GPT and ChatGPT](https://youtu.be/Lvhu0_y6K4E?list=PLmZlBIcArwhOVLRdimL3lS9F_33fzh9jU) (13 min)
- [Reinforcement learning from human feedback](https://youtu.be/T3DSOSea4yQ?list=PLmZlBIcArwhOVLRdimL3lS9F_33fzh9jU) (15 min)



# Speech recognition

- Encoder-decoder models for speech recognition:

    - Sec. 16.3 of
      ([Jurafsky and Martin 2025, Chap. 16](https://web.stanford.edu/~jurafsky/slp3/16.pdf))

- [Sequence modelling with CTC](https://distill.pub/2017/ctc/)

- CTC-based speech recognition:

    - Sec. 16.4 of
      ([Jurafsky and Martin 2025, Chap. 16](https://web.stanford.edu/~jurafsky/slp3/16.pdf))

- Evaluating speech recognition systems with word error rate:

    - Edit distance video above
    - Sec. 16.5 of
      ([Jurafsky and Martin 2025, Chap. 16](https://web.stanford.edu/~jurafsky/slp3/16.pdf))

- [HuBERT](https://arxiv.org/abs/2106.07447)
    
    - Read together
    - HuBERT forms the basis of many speech recognition models, but are also
      used as the basic feature extraction for unsupervised learning models and
      even speech synthesis systems.

- [wav2vec 2.0](https://arxiv.org/abs/2006.11477)

    This model is often used as the basis for speech recognition, e.g. on
    Hugging Face. A multilingual variant called XLSR
    ([Conneau et al., 2020](https://arxiv.org/abs/2006.13979)) is often used
    to initialise speech recognition models when targetting a new language.
 


# Speech synthesis

The terms "speech synthesis" and "text-to-speech" are sometimes used
interchangably.

- [Tacotron](https://arxiv.org/abs/1703.10135)

    - Caused the big shift towards neural speech synthesis

- Very attentative Tacotron (?)



# Future

- Explain what forced alignments are


# Further reading 

- [Hugging Face NLP tutorial](https://huggingface.co/learn/nlp-course/chapter1/1)
- [Hugging Face audio tutorial](https://huggingface.co/learn/audio-course/chapter0/introduction)
