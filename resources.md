---
layout: page
title: Resources
permalink: /resources/
order: 3
---

# Resources

### Code and data

Most of my code is available on [GitHub](https://github.com/{{ site.github_username }}). To find the code for a particular paper, it is probably easier to look for the `[code]` link given with each of papers on the [publications]({{site.url}}/publications/) page. But below I give a summary of some of the main repositories.

- **[YFACC](https://www.kamperh.com/yfacc)**: Yorùbá Flickr Audio Caption Corpus. The dataset is described in [(Olaleye et al., 2023)](https://arxiv.org/abs/2210.04600).
- **[globalphone_awe](https://github.com/kamperh/globalphone_awe)**: A complete recipe for the multilingual acoustic word embedding approach described in [(Kamper et al., 2020)](https://arxiv.org/abs/2002.02109). Embeddings are trained on one set of GlobalPhone languages and evaluated on another.
- **[recipe_bucktsong_awe_py3](https://github.com/kamperh/recipe_bucktsong_awe_py3)**: A complete recipe for the unsupervised acoustic word embedding methods described in [(Kamper, 2019)](https://arxiv.org/abs/1811.00403). Methods are evaluated on the Buckeye English and NCHLT Xitsonga datasets.
- **[recipe_semantic_flickraudio](https://github.com/kamperh/recipe_semantic_flickraudio)**: A complete recipe for our visually grounded semantic speech retrieval model described in [(Kamper et al., 2019)](https://arxiv.org/abs/1710.01949). This recipe uses the [semantic_flickraudio](https://github.com/kamperh/semantic_flickraudio) dataset below, and is an updated version of the [recipe_vision_speech_flickr](https://github.com/kamperh/recipe_vision_speech_flickr) recipe.
- **[semantic_flickraudio](https://github.com/kamperh/semantic_flickraudio)**: A dataset of labels for semantic speech retrieval, as described in [(Kamper et al., 2019)](https://arxiv.org/abs/1710.01949).  The dataset is an extension of the [Flickr Audio Captions Corpus](https://groups.csail.mit.edu/sls/downloads/flickraudio/) from MIT.
- **[ES-KMeans](https://github.com/kamperh/eskmeans)**: The embedded segmental K-means (ES-KMeans) algorithm for unsupervised word segmentation and clustering of speech in Python 3. We use it in [(Kamper et al., 2017)](https://arxiv.org/abs/1703.08135), as shown in this [recipe](https://github.com/kamperh/bucktsong_eskmeans).
- **[segmentalist](https://github.com/kamperh/segmentalist)**: Unsupervised word segmentation and clustering of speech in Python. We use it in [(Kamper et al., 2017)](https://arxiv.org/abs/1606.06950) and apply it to the Zero Resource Speech Challenge 2015 data (English and Xitsonga), as shown in this [complete recipe](https://github.com/kamperh/bucktsong_segmentalist).
- **[bayes_gmm](https://github.com/kamperh/bayes_gmm)**: Bayesian Gaussian mixture models in Python, as described in [(Kamper et al., 2014)]({{site.url}}/papers/kamper+jansen+king+goldwater_slt2014.pdf).


### Invited talks

- [Speech systems that emulate language acquisition in humans]({{site.url}}/slides/kamper_epfl2023_talk-compressed.pdf)  
  SDSC, École Polytechnique Fédérale de Lausanne, 2023.
- [Multimodal few-shot learning & probing self-supervised speech models]({{site.url}}/slides/kamper_ens2023_talk-compressed.pdf)  
  LSCP, Ecole Normale Supérieure, 2023.
- [What can large spoken language models tell us about speech?]({{site.url}}/slides/kamper_indabax2023_talk-compressed.pdf)  
  IndabaX South Africa, University of Cape Town, 2023.
- [Unsupervised word segmentation using dynamic programming on self-supervised speech representations]({{site.url}}/slides/kamper_aaaisas2022_talk.pdf)  
  AAAI SAS Workshop, Invited Talk, 2022. [[video](https://youtu.be/oA0EMR_cMQY)]
- [Learning acoustic units and words from unlabelled speech (with a bit of vision)]({{site.url}}/slides/kamper_jhuclsp2020_talk.pdf)  
  CLSP Seminar, Johns Hopkins University, 2020.
- [(Outrageously) low-resource speech processing]({{site.url}}/slides/kamper_indaba2019_talk.pdf)  
  Deep Learning Indaba, Nairobi, 2019. [[video](https://youtu.be/dTV4mbMJ9yM)]
- [Multimodal learning from images and speech]({{site.url}}/slides/kamper_leuvenupf_talk_2019.pdf)  
  Aalto University & Tampere University, 2019.  
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
  CSAIL, MIT, 2016.
- [Unsupervised speech processing using acoustic word embeddings]({{site.url}}/slides/kamper_mlslp2016_talk.pdf)  
  MLSLP Workshop, Spotlight Speaker, 2016.


### For Stellenbosch University students

- [Getting started with the Stellenbosch HPC](https://gist.github.com/RF5/eabb93ba85b763746d404afc9626e5d1) by Matthew Baas
- [Electrical and Electronic Engineering LaTeX template](https://github.com/kamperh/stellenbosch_ee_report_template)
