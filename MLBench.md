---
layout: proj
title: "ease.ml :: MLBench"
slogan: "MLBench: How Good Are Machine Learning Clouds for Binary Classification with Good Features?"
projname: "MLBench"
paperlink: "https://arxiv.org/abs/1707.09562"
paperbutton: ArXiv Full Version
---

<b>Abstract:</b> We conduct an empirical study of machine learning functionalities provided by major cloud service providers, which we call em machine learning clouds. Machine learning clouds hold the promise of hiding all the sophistication of running large-scale machine learning: Instead of specifying how to run a machine learning task, users only specify what machine learning task to run and the cloud figures out the rest. Raising the level of abstraction, however, rarely comes free --- a performance penalty is possible. How good, then, are current machine learning clouds on real-world machine learning workloads? 

We study this question by presenting mlbench, a novel benchmark dataset constructed with the top winning code for all available competitions on Kaggle, as well as the results we obtained by running mlbench on machine learning clouds from both Azure and Amazon. We analyze the strength and weakness of existing machine learning clouds and discuss potential future directions.

<!--<b><a href="http://ease.ml/res/gan_paper.pdf">Paper PDF</a></b>-->

# Methodology

In our study, we use a methodology that allows us to separate measuring the performance of the machine learning clouds themselves from other external factors that may have significant impact on quality, such as feature selection and hyper-parameter tuning. We use a performance metric that fairly measures the strength and weakness of current machine learning clouds by comparing their relative performance with top-ranked solutions in Kaggle competitions.

# MLBench

We constructed mlbench, a benchmark for evaluating machine learning models on the clouds. We collected all winning codes for Kaggle competitions that are available online. We then ran the winning code and used their feature engineering code to extract features. Those features are arguably the best features one can get, as the winners used them to win the Kaggle competitions. mlbench consists of 7 sets of features from 6 Kaggle competions. We restrict the scope of our study to binary classification. We plan to extend it to multi-class classification and regression and add more datasets to mlbench.

The MLBench dataset can be downloaded at: <a target="_blank" href="https://www.dropbox.com/s/31jol1wuz2mu2gf/MLbench.zip?dl=0">https://www.dropbox.com/s/31jol1wuz2mu2gf/MLbench.zip?dl=0</a>

# Results

We evaluate the two most popular machine learning clouds, Azure Machine Learning Stu- dio (Azure) and Amazon Machine Learning (Amazon), using mlbench. We find that: (1) Diversity of models is beneficial. Azure provides more alternative models than Amazon — Amazon only uses logistic regression for binary classification. Figure 1 suggests that the additional models provided by Azure help to achieve significant higher ranking; (2) Model selection is challenging. Using a different model can often lead to very different rankings. Although Azure provides more models to users, model selection is a difficult job for Azure users; and (3) Hyper-parameter tuning is time-consuming but beneficial. We use grid search to systematically explore hyper-parameters and observe huge variance of quality across different hyper-parameter settings.

# Learn More?

Check out the full version on ArXiv <a target="_blank" href="https://arxiv.org/abs/1707.09562">https://arxiv.org/abs/1707.09562</a>

