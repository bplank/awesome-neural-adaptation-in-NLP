# awesome-neural-adaptation-in-NLP 

[![MIT License](https://img.shields.io/badge/license-MIT-green.svg)](https://opensource.org/licenses/MIT) [![Awesome](https://cdn.rawgit.com/sindresorhus/awesome/d7305f38d29fed78fa85652e3a63e154dd8e8829/media/badge.svg)](https://github.com/sindresorhus/awesome)

A curated list of awesome work on neural unsupervised domain adaptation in Natural Language Processing, including links to papers. The focus is on *unsupervised* neural DA methods and currently on work outside Machine Translation. Feel free to contribute by creating a pull request as outlined in [contributing.md](contributing.md).

![taxonomy image](https://github.com/bplank/awesome-neural-adaptation-in-NLP-temp/blob/master/taxonomy.png?raw=true)

Please cite our [[survey paper]](https://arxiv.org/abs/2006.00632) (to appear in COLING 2020) if you find it useful in your research:
```
  @article{ramponi-and-plank-2020-neural,
      title={Neural Unsupervised Domain Adaptation in NLP---A Survey},
      author={Ramponi, Alan, and Plank, Barbara},
      year={2020},
      journal={arXiv preprint arXiv:2005.14672},
      eprint={2005.14672},
      archivePrefix={arXiv},
      primaryClass={cs.CL}
}
```

# Contents
- [Surveys](#surveys)
- [Collections](#collections)
- [Related Topics](#related-topics)

- [Unsupervised DA](#unsupervised-da)
  - [**By methods**](#by-methods)
    - [Model centric methods](#model-centric-methods)
      - [Feature-centric methods](#feature-centric)
      - [Loss-centric methods](#loss-centric)
    - [Data centric methods](#data-centric-methods)
      - [Pseudo labeling methods](#pseudo-labeling)
      - [Data selection methods](#data-selection)
      - [Pre-training methods](#pre-training)
    - [Hybrid methods](#hybrid-methods)
  - [**By tasks**](#by-tasks)
    - [Classification/inference](#classification-inference)
      - [Sentiment analysis](#sentiment-analysis)
      - [Language identification](#language-identification)
      - [Binary text classification](#binary-text-classification)
        - [Machine reading](#machine-reading)
        - [Duplicate question detection](#duplicate-question-detection)
        - [Stance detection](#stance-detection)
        - [Political data identification](#political-data-identification)
    - [Structured prediction](#structured-prediction)
      - [Natural language inference](#natural-language-inference)
      - [Part-of-speech tagging](#pos-tagging)
      - [Dependency parsing](#dependency-parsing)
      - [Named entity recognition](#named-entity-recognition)
      - [Relation extraction](#relation-extraction)





# Surveys

**Machine Learning**
- A Survey on Transfer Learning [[Pan & Yang, 2010, IEEE]](https://sci-hub.tw/10.1109/msp.2014.2347059&)

**Vision**
- Deep Visual Domain Adaptation: A Survey [[Wang & Deng, Neurocomputing 2018]](https://arxiv.org/abs/1802.03601v4)

**Machine Translation**
- A Survey of Domain Adaptation for Neural Machine Translation [[Chu & Wang, COLING 2018]](https://www.aclweb.org/anthology/C18-1111.pdf)

**Domain Adaptation in NLP**
- Domain Adaptation in Natural Language Processing [[Jiang, 2008; PhD dissertation, chapter 2]](https://www.ideals.illinois.edu/handle/2142/10870)
- A Literature Survey on Domain Adaptation of Statistical Classifiers [[Jiang, 2008, technical report]](http://www.mysmu.edu/faculty/jingjiang/papers/da_survey.pdf)
- Domain Adaptation for Parsing [[Plank, 2011; PhD dissertation, chapter 3]](https://www.rug.nl/research/portal/files/10469724/03c3.pdf)

**Transfer Learning for NLP**

- Neural Transfer Learning for NLP [[Ruder, 2019; PhD dissertation]](https://ruder.io/thesis/neural_transfer_learning_for_nlp.pdf)



# Collections

Related awesome collections:

- [awsome-domain-adaptation](https://github.com/zhaoxin94/awesome-domain-adaptation)
- [NLP progress page for domain adaptation](http://nlpprogress.com/english/domain_adaptation.html)
- [awesome-datascience](https://github.com/academic/awesome-datascience)
- [The-NLP-Pandect](https://github.com/bplank/The-NLP-Pandect)

# Related Topics

Surveys on related topics 

**Cross-Lingual Learning**
- A Survey of Cross-lingual Word Embedding Models [[Ruder, Vulić, Søgaard, JAIR 2019]](https://www.jair.org/index.php/jair/article/view/11640)

**Multi-task Learning**
- An Overview of Multi-Task Learning in Deep Neural Networks
[[Ruder, arXiv 2017]](https://arxiv.org/abs/1706.05098)


# Unsupervised DA

## By methods

A list of papers categorized by methods.

### Model centric methods

- Neural Structural Correspondence Learning for Domain Adaptation [[Ziser and Reichart, CoNLL 2017]](https://www.aclweb.org/anthology/K17-1040)
- Deep Pivot-Based Modeling for Cross-language Cross-Domain Transfer with Minimal Guidance [[Ziser and Reichart, EMNLP 2018a]](https://www.aclweb.org/anthology/D18-1022)
- Pivot Based Language Modeling for Improved Neural Domain Adaptation [[Ziser and Reichart, NAACL-HLT 2018b]](https://www.aclweb.org/anthology/N18-1112)
- Task Refinement Learning for Improved Accuracy and Stability of Unsupervised Domain Adaptation [[Ziser and Reichart, ACL 2019]](https://www.aclweb.org/anthology/P19-1591)
- Simplified Neural Unsupervised Domain Adaptation [[Miller, NAACL-HLT 2019]](https://www.aclweb.org/anthology/N19-1039)
- Domain Adaptation for Large-Scale Sentiment Classification: A Deep Learning Approach [[Glorot et al., ICML 2011]](https://icml.cc/2011/papers/342_icmlpaper.pdf)
- Marginalized Denoising Autoencoders for Domain Adaptation [[Chen et al., ICML 2012]](https://icml.cc/2012/papers/416.pdf)
- Fast Easy Unsupervised Domain Adaptation with Marginalized Structured Dropout [[Yang and Eisenstein, ACL 2014]](https://www.aclweb.org/anthology/P14-2088)
- A Domain Adaptation Regularization for Denoising Autoencoders [[Clinchant et al., ACL 2016]](https://www.aclweb.org/anthology/P16-2005/)
- Domain-Adversarial Training of Neural Networks [[Ganin et al., JMLR 2016]](https://jmlr.org/papers/volume17/15-239/15-239.pdf)
- End-to-End Adversarial Memory Network for Cross-domain Sentiment Classification [[Li et al., IJCAI 2017]](https://www.ijcai.org/Proceedings/2017/0311.pdf)
- Adversarial Adaptation of Synthetic or Stale Data [[Kim et al., ACL 2017]](https://www.aclweb.org/anthology/P17-1119)
- Adversarial Training for Cross-Domain Universal Dependency Parsing [[Sato et al., CoNLL 2017]](https://www.aclweb.org/anthology/K17-3007)
- Adversarial Training for Relation Extraction [[Wu et al., EMNLP 2017]](https://www.aclweb.org/anthology/D17-1187)
- Robust Multilingual Part-of-Speech Tagging via Adversarial Training [[Yasunaga et al., NAACL-HLT 2018]](https://www.aclweb.org/anthology/N18-1089)
- Wasserstein Distance Guided Representation Learning for Domain Adaptation [[Shen et al., AAAI 2018]](https://arxiv.org/abs/1707.01217)
- What's in a Domain? Learning Domain-Robust Text Representations using Adversarial Training [[Li et al., NAACL-HLT 2018]](https://www.aclweb.org/anthology/N18-2076)
- Domain Adaptation with Adversarial Training and Graph Embeddings [[Alam et al., ACL 2018]](https://www.aclweb.org/anthology/P18-1099)
- Adversarial Domain Adaptation for Machine Reading Comprehension [[Wang et al., EMNLP-IJCNLP 2019]](https://www.aclweb.org/anthology/D19-1254)
- Adversarial Domain Adaptation for Duplicate Question Detection [[Shah et al., EMNLP 2018]](https://www.aclweb.org/anthology/D18-1131)
- Domain Adaptation for Relation Extraction with Domain Adversarial Neural Network [[Fu et al., IJCNLP 2017]](https://www.aclweb.org/anthology/I17-2072)
- Generalizing Biomedical Relation Classification with Neural Adversarial Domain Adaptation [[Rios et al., Bioinf. 2018]](https://academic.oup.com/bioinformatics/article/34/17/2973/4953706)
- Adversarial Domain Adaptation for Stance Detection [[Xu et al., arXiv 2019]](https://arxiv.org/abs/1902.02401)
- Genre Separation Network with Adversarial Training for Cross-genre Relation Extraction [[Shi et al., EMNLP 2018]](https://www.aclweb.org/anthology/D18-1125)
- A Comparative Analysis of Unsupervised Language Adaptation Methods [[Rocha, Lopes Cardoso, DeepLo 2019]](https://www.aclweb.org/anthology/D19-6102)
- KinGDOM: Knowledge-Guided DOMain Adaptation for Sentiment Analysis [[Ghosal et al., ACL 2020]](https://www.aclweb.org/anthology/2020.acl-main.292)
- Towards Open Domain Event Trigger Identification using Adversarial Domain Adaptation [[Naik, Rose, ACL 2020]](https://www.aclweb.org/anthology/2020.acl-main.681)

### Data centric methods

- Unsupervised Domain Adaptation of Contextualized Embeddings for Sequence Labeling [[Han, Eisenstein, EMNLP-IJCNLP 2019]](https://www.aclweb.org/anthology/D19-1433)
- Semi-supervised Domain Adaptation for Dependency Parsing [[Li et al., ACL 2019]](https://www.aclweb.org/anthology/P19-1229)
- Adaptive Ensembling: Unsupervised Domain Adaptation for Political Document Analysis [[Desai et al., EMNLP-IJCNLP 2019]](https://www.aclweb.org/anthology/D19-1478)
- Don't Stop Pretraining: Adapt Language Models to Domains and Tasks [[Gururangan et al., ACL 2020]](https://www.aclweb.org/anthology/2020.acl-main.740/)

### Hybrid methods

- Asymmetric Tri-training for Unsupervised Domain Adaptation [[Saito et al., ICML 2017]](http://proceedings.mlr.press/v70/saito17a.html)
- Strong Baselines for Neural Semi-Supervised Learning under Domain Shift [[Ruder, Plank, ACL 2018]](https://www.aclweb.org/anthology/P18-1096)
- Cross-Domain NER using Cross-Domain Language Modeling [[Jia et al., ACL 2019]](https://www.aclweb.org/anthology/P19-1236)
- Deep Contextualized Self-Training for Low Resource Dependency Parsing [[Rotman, Reichart, TACL 2019]](https://www.mitpressjournals.org/doi/full/10.1162/tacl_a_00294)
- Self-Adaptation for Unsupervised Domain Adaptation [[Cui, Bollegala, RANLP 2019]](https://www.aclweb.org/anthology/R19-1025)
- Multi-Task Domain Adaptation for Sequence Tagging [[Peng, Dredze, RepL4NLP 2017]](https://www.aclweb.org/anthology/W17-2612)
- Multi-Source Domain Adaptation for Text Classification via DistanceNet-Bandits [[Guo et al., AAAI(?) 2020]](https://arxiv.org/abs/2001.04362)
- PERL: Pivot-Based Domain Adaptation for Pre-Trained Deep Contextualized Embedding Models [[Ben-David et al., TACL 2020]](https://arxiv.org/abs/2006.09075)

## By tasks

A list of papers categorized by tasks.

### Classification/inference

All papers pertaining to classification and inference tasks are indicated in the respective sections below.

#### Sentiment analysis

- Neural Structural Correspondence Learning for Domain Adaptation [[Ziser and Reichart, CoNLL 2017]](https://www.aclweb.org/anthology/K17-1040)
- Deep Pivot-Based Modeling for Cross-language Cross-Domain Transfer with Minimal Guidance [[Ziser and Reichart, EMNLP 2018a]](https://www.aclweb.org/anthology/D18-1022)
- Pivot Based Language Modeling for Improved Neural Domain Adaptation [[Ziser and Reichart, NAACL-HLT 2018b]](https://www.aclweb.org/anthology/N18-1112)
- Task Refinement Learning for Improved Accuracy and Stability of Unsupervised Domain Adaptation [[Ziser and Reichart, ACL 2019]](https://www.aclweb.org/anthology/P19-1591)
- Simplified Neural Unsupervised Domain Adaptation [[Miller, NAACL-HLT 2019]](https://www.aclweb.org/anthology/N19-1039)
- Domain Adaptation for Large-Scale Sentiment Classification: A Deep Learning Approach [[Glorot et al., ICML 2011]](https://icml.cc/2011/papers/342_icmlpaper.pdf)
- Marginalized Denoising Autoencoders for Domain Adaptation [[Chen et al., ICML 2012]](https://icml.cc/2012/papers/416.pdf)
- A Domain Adaptation Regularization for Denoising Autoencoders [[Clinchant et al., ACL 2016]](https://www.aclweb.org/anthology/P16-2005/)
- Domain-Adversarial Training of Neural Networks [[Ganin et al., JMLR 2016]](https://jmlr.org/papers/volume17/15-239/15-239.pdf)
- End-to-End Adversarial Memory Network for Cross-domain Sentiment Classification [[Li et al., IJCAI 2017]](https://www.ijcai.org/Proceedings/2017/0311.pdf)
- Wasserstein Distance Guided Representation Learning for Domain Adaptation [[Shen et al., AAAI 2018]](https://arxiv.org/abs/1707.01217)
- What's in a Domain? Learning Domain-Robust Text Representations using Adversarial Training [[Li et al., NAACL-HLT 2018]](https://www.aclweb.org/anthology/N18-2076)
- A Comparative Analysis of Unsupervised Language Adaptation Methods [[Rocha, Lopes Cardoso, DeepLo 2019]](https://www.aclweb.org/anthology/D19-6102)
- KinGDOM: Knowledge-Guided DOMain Adaptation for Sentiment Analysis [[Ghosal et al., ACL 2020]](https://www.aclweb.org/anthology/2020.acl-main.292)
- Don't Stop Pretraining: Adapt Language Models to Domains and Tasks [[Gururangan et al., ACL 2020]](https://www.aclweb.org/anthology/2020.acl-main.740/)
- Asymmetric Tri-training for Unsupervised Domain Adaptation [[Saito et al., ICML 2017]](http://proceedings.mlr.press/v70/saito17a.html)
- Strong Baselines for Neural Semi-Supervised Learning under Domain Shift [[Ruder, Plank, ACL 2018]](https://www.aclweb.org/anthology/P18-1096)
- Self-Adaptation for Unsupervised Domain Adaptation [[Cui, Bollegala, RANLP 2019]](https://www.aclweb.org/anthology/R19-1025)
- Multi-Source Domain Adaptation for Text Classification via DistanceNet-Bandits [[Guo et al., AAAI 2020]](https://arxiv.org/abs/2001.04362)
- PERL: Pivot-Based Domain Adaptation for Pre-Trained Deep Contextualized Embedding Models [[Ben-David et al., TACL 2020]](https://arxiv.org/abs/2006.09075)

#### Language identification

- What's in a Domain? Learning Domain-Robust Text Representations using Adversarial Training [[Li et al., NAACL-HLT 2018]](https://www.aclweb.org/anthology/N18-2076)

#### Binary text classification

- A Domain Adaptation Regularization for Denoising Autoencoders [[Clinchant et al., ACL 2016]](https://www.aclweb.org/anthology/P16-2005/)
- Adversarial Adaptation of Synthetic or Stale Data [[Kim et al., ACL 2017]](https://www.aclweb.org/anthology/P17-1119)
- Domain Adaptation with Adversarial Training and Graph Embeddings [[Alam et al., ACL 2018]](https://www.aclweb.org/anthology/P18-1099)
- Don't Stop Pretraining: Adapt Language Models to Domains and Tasks [[Gururangan et al., ACL 2020]](https://www.aclweb.org/anthology/2020.acl-main.740/)

##### Machine reading

- Adversarial Domain Adaptation for Machine Reading Comprehension [[Wang et al., EMNLP-IJCNLP 2019]](https://www.aclweb.org/anthology/D19-1254)

##### Duplicate question detection

- Adversarial Domain Adaptation for Duplicate Question Detection [[Shah et al., EMNLP 2018]](https://www.aclweb.org/anthology/D18-1131)

##### Stance detection

- Adversarial Domain Adaptation for Stance Detection [[Xu et al., arXiv 2019]](https://arxiv.org/abs/1902.02401)

##### Political data identification

- Adaptive Ensembling: Unsupervised Domain Adaptation for Political Document Analysis [[Desai et al., EMNLP-IJCNLP 2019]](https://www.aclweb.org/anthology/D19-1478)

### Structured prediction

All papers pertaining to structured prediction tasks are indicated in the respective sections below.

#### Natural language inference

- A Comparative Analysis of Unsupervised Language Adaptation Methods [[Rocha, Lopes Cardoso, DeepLo 2019]](https://www.aclweb.org/anthology/D19-6102)
- Don't Stop Pretraining: Adapt Language Models to Domains and Tasks [[Gururangan et al., ACL 2020]](https://www.aclweb.org/anthology/2020.acl-main.740/)

#### Part-of-speech tagging

- Fast Easy Unsupervised Domain Adaptation with Marginalized Structured Dropout [[Yang and Eisenstein, ACL 2014]](https://www.aclweb.org/anthology/P14-2088)
- Robust Multilingual Part-of-Speech Tagging via Adversarial Training [[Yasunaga et al., NAACL-HLT 2018]](https://www.aclweb.org/anthology/N18-1089)
- Unsupervised Domain Adaptation of Contextualized Embeddings for Sequence Labeling [[Han, Eisenstein, EMNLP-IJCNLP 2019]](https://www.aclweb.org/anthology/D19-1433)
- Strong Baselines for Neural Semi-Supervised Learning under Domain Shift [[Ruder, Plank, ACL 2018]](https://www.aclweb.org/anthology/P18-1096)
- Multi-Task Domain Adaptation for Sequence Tagging [[Peng, Dredze, RepL4NLP 2017]](https://www.aclweb.org/anthology/W17-2612)

#### Dependency parsing

- Adversarial Training for Cross-Domain Universal Dependency Parsing [[Sato et al., CoNLL 2017]](https://www.aclweb.org/anthology/K17-3007)
- Semi-supervised Domain Adaptation for Dependency Parsing [[Li et al., ACL 2019]](https://www.aclweb.org/anthology/P19-1229)
- Deep Contextualized Self-Training for Low Resource Dependency Parsing [[Rotman, Reichart, TACL 2019]](https://www.mitpressjournals.org/doi/full/10.1162/tacl_a_00294)

#### Named entity recognition

- Adversarial Adaptation of Synthetic or Stale Data [[Kim et al., ACL 2017]](https://www.aclweb.org/anthology/P17-1119)
- Towards Open Domain Event Trigger Identification using Adversarial Domain Adaptation [[Naik, Rose, ACL 2020]](https://www.aclweb.org/anthology/2020.acl-main.681)
- Unsupervised Domain Adaptation of Contextualized Embeddings for Sequence Labeling [[Han, Eisenstein, EMNLP-IJCNLP 2019]](https://www.aclweb.org/anthology/D19-1433)
- Cross-Domain NER using Cross-Domain Language Modeling [[Jia et al., ACL 2019]](https://www.aclweb.org/anthology/P19-1236)
- Multi-Task Domain Adaptation for Sequence Tagging [[Peng, Dredze, RepL4NLP 2017]](https://www.aclweb.org/anthology/W17-2612)

#### Relation extraction

- Adversarial Training for Relation Extraction [[Wu et al., EMNLP 2017]](https://www.aclweb.org/anthology/D17-1187)
- Domain Adaptation for Relation Extraction with Domain Adversarial Neural Network [[Fu et al., IJCNLP 2017]](https://www.aclweb.org/anthology/I17-2072)
- Generalizing Biomedical Relation Classification with Neural Adversarial Domain Adaptation [[Rios et al., Bioinf. 2018]](https://academic.oup.com/bioinformatics/article/34/17/2973/4953706)
- Genre Separation Network with Adversarial Training for Cross-genre Relation Extraction [[Shi et al., EMNLP 2018]](https://www.aclweb.org/anthology/D18-1125)
- Don't Stop Pretraining: Adapt Language Models to Domains and Tasks [[Gururangan et al., ACL 2020]](https://www.aclweb.org/anthology/2020.acl-main.740/)
