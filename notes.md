---
layout: page
title: Resources
permalink: /resources/
order: 1
---

# Resources

### Notes

Hopefully someone else might also find these notes useful. Let me know if you find any mistakes or have any comments.

- [Yet another introduction to backpropagation]({{site.url}}/notes/kamper_backprop17.pdf)
- [Gibbs sampling for fitting finite and infinite Gaussian mixture models]({{site.url}}/notes/kamper_bayesgmm15.pdf)
  [[code](https://github.com/kamperh/bayes_gmm)]
- [Vector and matrix calculus]({{site.url}}/notes/kamper_matrixcalculus13.pdf).


### Invited talks

- [Deep learning for (more than) speech recognition]({{site.url}}/slides/kamper_indabax2018_talk.pdf)  
  IndabaX Western Cape, UCT, 2018. [[video](https://youtu.be/lvQipmlgDFY)]
- [Learning from unlabelled speech, with and without visual cues]({{site.url}}/slides/kamper_unsup_visionspeech_talk_2017.pdf)  
  Ohio State University, 2017.
- [Learning from unlabelled speech, with and without visual cues]({{site.url}}/slides/kamper_unsup_visionspeech_talk_2017.pdf)  
  University of Maryland, CLIP Colloquium Speaker, 2017.
- [Unsupervised neural and Bayesian models for zero-resource speech processing]({{site.url}}/slides/kamper_mit2016_talk.pdf)  
  MIT, Computer Science and Artificial Intelligence Laboratory, 2016.
- [Unsupervised speech processing using acoustic word embeddings]({{site.url}}/slides/kamper_mlslp2016_talk.pdf)  
  Workshop on Machine Learning in Speech and Language Processing, Spotlight Speaker, 2016.


### Code and data

Most of my code is available on [GitHub](https://github.com/{{ site.github_username }}), as also noted with each of the [publications]({{site.url}}/publications/). Below is a summary of some of the main repositories.

- **[semantic_flickraudio](https://github.com/kamperh/semantic_flickraudio)**: A dataset of labels for semantic speech retrieval, as described in [arXiv'17](https://arxiv.org/abs/1710.01949).  The dataset is an extension of the [Flickr Audio Captions Corpus](https://groups.csail.mit.edu/sls/downloads/flickraudio/) from MIT.
- **[recipe_vision_speech_flickr](https://github.com/kamperh/recipe_vision_speech_flickr)**: A complete recipe for our visually grounded keyword prediction model described in [Interspeech'17](https://arxiv.org/abs/1703.08136).
- **[segmentalist](https://github.com/kamperh/segmentalist)**: Unsupervised word segmentation and clustering of speech in Python. We use it in [CSL'17](https://arxiv.org/abs/1606.06950) and apply it to the Zero Resource Speech Challenge 2015 data (English and Xitsonga), as shown in this [complete recipe](https://github.com/kamperh/bucktsong_segmentalist).
- **[couscous](https://github.com/kamperh/couscous)**:  Theano code for training Siamese CNNs. We used it in [ICASSP'16]({{site.url}}/papers/kamper+wang+livescu_icassp2016.pdf) for training acoustic word embeddings from speech, as shown in this [complete recipe](https://github.com/kamperh/recipe_swbd_wordembeds).
- **[speech_correspondence](https://github.com/kamperh/speech_correspondence)**: Pylearn2 implementation of the correspondence autoencoder, as described in [ICASSP'15]({{site.url}}/papers/kamper+elsner+jansen+goldwater_icassp2015.pdf).
- **[bayes_gmm](https://github.com/kamperh/bayes_gmm)**: Bayesian Gaussian mixture models in Python, as described in [SLT'14]({{site.url}}/papers/kamper+jansen+king+goldwater_slt2014.pdf).
