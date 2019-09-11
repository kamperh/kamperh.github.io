---
layout: page
title: Resources
permalink: /resources/
order: 1
---

# Resources

### Notes and notebooks

Hopefully someone else might also find these notes useful. Let me know if you find any mistakes or have any comments.

- [Yet another introduction to backpropagation]({{site.url}}/notes/kamper_backprop17.pdf)
- [Gibbs sampling for fitting finite and infinite Gaussian mixture models]({{site.url}}/notes/kamper_bayesgmm15.pdf)
  [[code](https://github.com/kamperh/bayes_gmm)]
- [Vector and matrix calculus]({{site.url}}/notes/kamper_matrixcalculus13.pdf)
- [Notebook: Autoencoder, variational AE, vector-quantised VAE, and categorical VAE on MNIST](https://github.com/kamperh/autoencoders_mnist/blob/master/ae_mnist.ipynb)


### Invited talks

- [Multimodal learning from
images and speech]({{site.url}}/slides/kamper_leuvenupf_talk_2019.pdf)  
  Aalto University & Tampere University, Finland, 2019.  
  KU Leuven & UPF Barcelona, 2019.
- [Acoustic word embeddings for low resource speech processing](https://twimlai.com/twiml-talk-191-acoustic-word-embeddings-for-low-resource-speech-processing-with-herman-kamper/)  
  TWiML&AI Podcast, 2018.
- [Frontiers of natural language processing]({{site.url}}/slides/ruder+kamper_indaba2018_talk.pdf)  
  With Sebastian Ruder. Deep Learning Indaba, Stellenbosch, 2018.
- [Deep learning for (more than) speech recognition]({{site.url}}/slides/kamper_indabax2018_talk.pdf)  
  IndabaX Western Cape, University of Cape Town, 2018. [[video](https://youtu.be/lvQipmlgDFY)]
- [Learning from unlabelled speech, with and without visual cues]({{site.url}}/slides/kamper_unsup_visionspeech_talk_2017.pdf)  
  Ohio State University, 2017.  
  CLIP Colloquium Speaker, University of Maryland, 2017.
- [Unsupervised neural and Bayesian models for zero-resource speech processing]({{site.url}}/slides/kamper_mit2016_talk.pdf)  
  Computer Science and Artificial Intelligence Laboratory, MIT, 2016.
- [Unsupervised speech processing using acoustic word embeddings]({{site.url}}/slides/kamper_mlslp2016_talk.pdf)  
  Spotlight Speaker, Workshop on Machine Learning in Speech and Language Processing, 2016.


### Code and data

Most of my code is available on [GitHub](https://github.com/{{ site.github_username }}). To find the code for a particular paper, it is probably easier to look for the `[code]` link given with each of papers on the [publications]({{site.url}}/publications/) page. But below I give summary of some of the main repositories.

- **[recipe_bucktsong_awe_py3](https://github.com/kamperh/recipe_bucktsong_awe_py3)**: A complete recipe for the unsupervised acoustic word embedding methods described in [ICASSP'19](https://arxiv.org/abs/1811.00403). Methods are evaluated on the Buckeye English and NCHLT Xitsonga datasets.
- **[recipe_semantic_flickraudio](https://github.com/kamperh/recipe_semantic_flickraudio)**: A complete recipe for our visually grounded semantic speech retrieval model described in [TASLP'18](https://arxiv.org/abs/1710.01949). This recipe uses the [semantic_flickraudio](https://github.com/kamperh/semantic_flickraudio) dataset below, and is an updated version of the [recipe_vision_speech_flickr](https://github.com/kamperh/recipe_vision_speech_flickr) recipe (also below).
- **[semantic_flickraudio](https://github.com/kamperh/semantic_flickraudio)**: A dataset of labels for semantic speech retrieval, as described in [arXiv'17](https://arxiv.org/abs/1710.01949).  The dataset is an extension of the [Flickr Audio Captions Corpus](https://groups.csail.mit.edu/sls/downloads/flickraudio/) from MIT.
- **[recipe_vision_speech_flickr](https://github.com/kamperh/recipe_vision_speech_flickr)**: A complete recipe for our visually grounded keyword prediction model described in [Interspeech'17](https://arxiv.org/abs/1703.08136). The [recipe_semantic_flickraudio](https://github.com/kamperh/recipe_semantic_flickraudio) repository above is an updated version of this recipe.
- **[segmentalist](https://github.com/kamperh/segmentalist)**: Unsupervised word segmentation and clustering of speech in Python. We use it in [CSL'17](https://arxiv.org/abs/1606.06950) and apply it to the Zero Resource Speech Challenge 2015 data (English and Xitsonga), as shown in this [complete recipe](https://github.com/kamperh/bucktsong_segmentalist).
- **[couscous](https://github.com/kamperh/couscous)**:  Theano code for training Siamese CNNs. We used it in [ICASSP'16]({{site.url}}/papers/kamper+wang+livescu_icassp2016.pdf) for training acoustic word embeddings from speech, as shown in this [complete recipe](https://github.com/kamperh/recipe_swbd_wordembeds).
- **[speech_correspondence](https://github.com/kamperh/speech_correspondence)**: Pylearn2 implementation of the correspondence autoencoder, as described in [ICASSP'15]({{site.url}}/papers/kamper+elsner+jansen+goldwater_icassp2015.pdf).
- **[bayes_gmm](https://github.com/kamperh/bayes_gmm)**: Bayesian Gaussian mixture models in Python, as described in [SLT'14]({{site.url}}/papers/kamper+jansen+king+goldwater_slt2014.pdf).
