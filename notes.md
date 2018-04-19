---
layout: page
title: Resources
permalink: /resources/
order: 1
---

# Resources

<!--
### Notes

Hopefully someone else might also find these notes useful. Let me know if you find any mistakes or have any comments.

- [Yet another introduction to backpropagation]({{site.url}}/notes/kamper_backprop17.pdf)
- [Gibbs sampling for fitting finite and infinite Gaussian mixture models]({{site.url}}/notes/kamper_bayesgmm15.pdf)
  [[code](https://github.com/kamperh/bayes_gmm)]
- [Vector and matrix calculus]({{site.url}}/notes/kamper_matrixcalculus13.pdf)
-->

### Notes

Hopefully someone else might also find these notes useful. Let me know if you find any mistakes or have any comments.

- Yet another introduction to backpropagation. [[pdf]({{site.url}}/notes/kamper_backprop17.pdf)]
- Gibbs sampling for fitting finite and infinite Gaussian mixture models.
  [[pdf]({{site.url}}/notes/kamper_bayesgmm15.pdf), [code](https://github.com/kamperh/bayes_gmm)]
- Vector and matrix calculus.
  [[pdf]({{site.url}}/notes/kamper_matrixcalculus13.pdf)]


### Invited talks

- *Deep learning for (more than) speech recognition.* IndabaX Western Cape, UCT, 2018. [[slides]({{site.url}}/slides/kamper_indabax2018_talk.pdf)]
- *Learning from unlabelled speech, with and without visual cues.* Ohio State University, 2017. [[slides]({{site.url}}/slides/kamper_unsup_visionspeech_talk_2017.pdf)]
- *Learning from unlabelled speech, with and without visual cues.* University of Maryland, CLIP Colloquium Speaker, 2017.
- *Unsupervised neural and Bayesian models for zero-resource speech processing.* MIT, Computer Science and Artificial Intelligence Laboratory, 2016. [[slides]({{site.url}}/slides/kamper_mit2016_talk.pdf)]
- *Unsupervised speech processing using acoustic word embeddings.* Workshop on Machine Learning in Speech and Language Processing, Spotlight Speaker, 2016. [[slides]({{site.url}}/slides/kamper_mlslp2016_talk.pdf)]


### Code

Most of my code is available on [GitHub](https://github.com/{{ site.github_username }}), as also noted with each of the [publications]({{site.url}}/publications/). Below is a summary of some of the main repositories.

- [recipe_vision_speech_flickr](https://github.com/kamperh/recipe_vision_speech_flickr): A complete recipe for our visually grounded keyword prediction model described in [Interspeech'17](https://arxiv.org/abs/1703.08136).
- [segmentalist](https://github.com/kamperh/segmentalist): Unsupervised word segmentation and clustering of speech in Python. We use it in [CSL'17](https://arxiv.org/abs/1606.06950) and apply it to the Zero Resource Speech Challenge 2015 data (English and Xitsonga), as shown in this [complete recipe](https://github.com/kamperh/bucktsong_segmentalist).
- [couscous](https://github.com/kamperh/couscous):  Theano code for training Siamese CNNs. We used it in [ICASSP'16]({{site.url}}/papers/kamper+wang+livescu_icassp2016.pdf) for training acoustic word embeddings from speech, as shown in this [complete recipe](https://github.com/kamperh/recipe_swbd_wordembeds).
- [speech_correspondence](https://github.com/kamperh/speech_correspondence): Pylearn2 implementation of the correspondence autoencoder, as described in [ICASSP'15]({{site.url}}/papers/kamper+elsner+jansen+goldwater_icassp2015.pdf).
- [bayes_gmm](https://github.com/kamperh/bayes_gmm): Bayesian Gaussian mixture models in Python, as described in [SLT'14]({{site.url}}/papers/kamper+jansen+king+goldwater_slt2014.pdf).
