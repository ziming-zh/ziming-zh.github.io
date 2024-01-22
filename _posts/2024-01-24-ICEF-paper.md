---
layout: post
title: Paper:Data-Driven Detection and Prediction of Spray Collapse Characteristics for Multi-Component Fuel Mixtures
categories: [Research]
tags: [Accepted Papers, Research]
date: '2024-01-21 15:56:38 -0600'
img_path: /assets/img/post/
---
<script type="text/x-mathjax-config">
MathJax.Hub.Config({
  tex2jax: {inlineMath: [['$','$'], ['\\(','\\)']]}
});
</script>
<script type="text/javascript" async src="https://cdnjs.cloudflare.com/ajax/libs/mathjax/2.7.5/MathJax.js?config=TeX-AMS_CHTML"></script>


> The paper is now available online at [10.1115/ICEF2023-110017](https://asmedigitalcollection.asme.org/ICEF/proceedings/ICEF2023/87561/V001T03A003/1194245)
{: .prompt-info }

## Paper Info

Date: January 2024

DOI: 10.1115/ICEF2023-110017

Conference: 2023 ASME Internal Combustion Engine Forward Conference

At: Pittsburg, PA, USA

Authors: Fengnian Zhao, <u>Ziming Zhou</u>, Weisong Liu, David L.S. Hung*

## Main Content 

### Research Background:


Flash boiling spray improves the quality of fuel atomization while also increasing the occurrence of spray collapse. The spray collapse phenomenon significantly increases the likelihood of unintended spray-wall impingement, thus reducing combustion stability. Therefore, this study focuses on the spray collapse states under flash boiling conditions and implements machine learning methods to enhance spray analysis including collapse pattern recognition and prediction. 

<center>
    <img style="border-radius: 0.3125em;
    box-shadow: 0 2px 4px 0 rgba(34,36,38,.12),0 2px 10px 0 rgba(34,36,38,.08);" 
    src="ICEFpaper-1.png" alt="Image failed to load">
    <br>
    <div style="color:orange; border-bottom: 1px solid #d9d9d9;
    display: inline-block;
    color: #999;
    padding: 2px;">  Background: flash-boiling & spray Collapse </div>
</center>


### Main Content: 


As a continuity of our previous work, the spray collapse characteristics of three-component surrogate fuels with various proportions of n-pentane, iso-octane, and n-decane are investigated using a planar laser Mie-scattering system. A production six-hole gasoline direct injection (GDI) injector is used in these experiments. To better reveal the transition from conventional spray behavior to flash boiling spray behavior, a wide range of subcooled and superheated conditions are examined. Based on the large amount of spray data as well as working conditions, this study aims to develop a data-driven framework to achieve two goals: 
1) to detect the spray collapse state from enormous spray images;
2) to predict the spray collapse state with given working conditions. 

<center>
    <img style="border-radius: 0.3125em;
    box-shadow: 0 2px 4px 0 rgba(34,36,38,.12),0 2px 10px 0 rgba(34,36,38,.08);" 
    src="ICEFpaper-2.png" alt="Image failed to load">
    <br>
    <div style="color:orange; border-bottom: 1px solid #d9d9d9;
    display: inline-block;
    color: #999;
    padding: 2px;">  Previous work & approaches </div>
</center>

The analysis framework in this study includes two steps in terms of (1) spray state detection and (2) spray state prediction. Figure 4 depicts the work flow of this framework. For a large amount of spray images, supervised ResNet model is first applied for spray state detection. As mentioned, the spray cross patterns are divided into three states of non-collapse state, transition state and collapse state. Therefore, the step of spray state detection is a classification task. With a well-trained ResNet model, the spray state can be identified automatically instead of manually distinguishing the images. After spray state detection, the feature importance of experimental parameters (including test and fuel parameters) is evaluated by DTC model. The principle of feature selection is to find the relevant features and remove the irrelevant ones. For spray measurements in this study, two categories of factors directly decide the spray behaviors: test conditions and test fuels. Therefore, the feature set includes fuel temperature, ambient pressure and fuel component proportions of n-decane, iso-octane, and n-pentane. The above parameters are closely related to the flash boiling behavior of sprays and further influence the spray collapse. Thus, the DTC model can be applied as the next step to evaluate the importance of these given features. The advantage of DTC is the clear and readable decision-making process, which can help us understand what the most important features are regarding spray collapse behavior. Finally, with a well-trained DTC model, spray collapse states can be predicted based on test and fuel parameters even for untested conditions. 

<center>
    <img style="border-radius: 0.3125em;
    box-shadow: 0 2px 4px 0 rgba(34,36,38,.12),0 2px 10px 0 rgba(34,36,38,.08);" 
    src="ICEFpaper-2-1.png" alt="Image failed to load">
    <br>
    <div style="color:orange; border-bottom: 1px solid #d9d9d9;
    display: inline-block;
    color: #999;
    padding: 2px;">  Analysis methodology - classification + prediction </div>
</center>

For spray measurements in this study, two categories of factors directly decide the spray behaviors: test conditions and test fuels. Therefore, the feature set includes fuel temperature, ambient pressure and fuel component proportions of $\mathrm{n}$-decane, iso-octane, and $\mathrm{n}$-pentane. Besides for these features, the superheated degree $P_a / P_b$ and its modified parameters, $K_1$. $\left(P_a / P_b\right)$ and $\left(K_1 / K_2\right) \cdot\left(P_a / P_b\right)$ are added to the feature set as well. Here $P_a$ represents ambient pressure; $P_b$ represents bubble point pressure; $K_1$ is an original parameter to eliminate the influence of ambient gas density; $K_2$ is an original parameter to eliminate the difference between $P_a / P_b$ for multi-component fuel spray and $P_a / P_s$ for single-component fuel spray. $K_1$ and $K_2$ are the important coefficients in our newly proposed superheated index for multi-component fuel spray $\left(K_1 / K_2\right) \cdot\left(P_a / P_b\right)$

<center>
    <img style="border-radius: 0.3125em;
    box-shadow: 0 2px 4px 0 rgba(34,36,38,.12),0 2px 10px 0 rgba(34,36,38,.08);" 
    src="ICEFpaper-3.png" alt="Image failed to load">
    <br>
    <div style="color:orange; border-bottom: 1px solid #d9d9d9;
    display: inline-block;
    color: #999;
    padding: 2px;">  Introducing modified superheated degree for multi-component fuel </div>
</center>


After classifying the spray collapse states into non-collapse state, transition state, and collapse state, the DTC models are implemented to regress the relationship between experimental parameters and spray collapse state. In this work, four DTC models with different feature subsets are trained and tested. The whole data-set includes 270 test cases with fifteen different test fuels, three ambient pressures and six fuel temperatures. The whole data-set is divided into two parts, training set with 75 % test cases (202 cases) and test set with 25 % test cases (68 cases). 

<center>
    <img style="border-radius: 0.3125em;
    box-shadow: 0 2px 4px 0 rgba(34,36,38,.12),0 2px 10px 0 rgba(34,36,38,.08); width: 50%; display: block; margin-left: auto; margin-right: auto;" 
    src="ICEFpaper-4.png" alt="Image failed to load">
    <br>
    <div style="color:orange; border-bottom: 1px solid #d9d9d9;
    display: inline-block;
    color: #999;
    padding: 2px;">  DTC models with different input features A-E </div>
</center>



**TABLE** **:** DTC MODEL PAREMETERS (FIVE BASIC PARAMETERS: AMBIENT PRESSURE, FUEL TEMPERATURE AND THE FUEL PROPORTIONS)

| DTCs    | Feature subset        | Maximum depth | Tree structure |
| ------- | --------------------- | ------------- | -------------- |
| Model A | 5 basic  parameters   | 1 ~ 11        | Binary         |
| Model B | 5 basic  parameters & $\left(P_a / P_b\right)$ | 1 ~ 11        | Binary         |
| Model C | 5 basic  parameters & $K_1$. $\left(P_a / P_b\right)$ | 1 ~ 11        | Binary         |
| Model D | 5 basic  parameters & $\left(K_1 / K_2\right) \cdot\left(P_a / P_b\right)$ | 1 ~ 11        | Binary         |


In DTC models, feature importance is calculated as the decrease in node impurity weighted by the probability of reaching that node. In DTC models, feature importance refers to assigning a score to input features based on how useful they are at predicting a target variable. Feature importance is calculated as the decrease in node impurity. For each feature, the value of its importance is between 0 and 1. 0 represents ‘not selected’ and 1 represents ‘perfect prediction’. The sum of all feature importance values is equal to 1. 

As shown in the following figure, the histogram shows ambient pressure, fuel temperature, and the proportion of n-pentane are top three features with around 0.3 feature importance. The result suggests the DTC model needs more steps in order to take more than one feature into consideration when deciding the spray collapse states. When $P_a / P_b$ is added into the feature subset, $P_a / P_b$ has the highest value of feature importance, above 0.8 . It suggests that this feature could indicates the spray collapse states more directly compared with other features. The similar effect of $K_1 \cdot\left(P_a / P_b\right)$ is shown in *Model C*. The only second important feature is npentane, which suggests the value of $K_1 \cdot\left(P_a / P_b\right)$ is not suitable for all test fuels. The most extreme cases are shown in *Model d* when $\left(K_1 / K_2\right) \cdot\left(P_a / P_b\right)$ is selected. The feature importance of $\left(K_1 / K_2\right) \cdot\left(P_a / P_b\right)$ is 1 , which means the model can predict spray collapse states based on this feature only. According to the results, the value of $\left(K_1 / K_2\right) \cdot\left(P_a / P_b\right)$ indicates spray collapse characteristics well and it can be used to predict spray collapse states.

<center>
    <img style="border-radius: 0.3125em;
    box-shadow: 0 2px 4px 0 rgba(34,36,38,.12),0 2px 10px 0 rgba(34,36,38,.08);" 
    src="ICEFpaper-4-1.png" alt="Image failed to load">
    <br>
    <div style="color:orange; border-bottom: 1px solid #d9d9d9;
    display: inline-block;
    color: #999;
    padding: 2px;">  Feature importance evaluation of DTC model A-D </div>
</center>

Through the prediction results from well-established DTC model D, the key take-away is that the proportion of n-pentane dominates the spray collapse behavior. The difference in spray collapse behavior is due to the fact that light fuels have relatively higher vapor pressure and therefore preferentially vaporize. In this work, n-pentane has the highest vapor pressure. Vaporization of n-pentane enhances plume-to-plume interactions, so high proportion of n-pentane can easily lead to spray collapse. Furthermore, for any multi-component fuels, the spray collapse behavior is strongly governed by the proportion of the component with highest vapor pressure. Using the DTC framework in this study, the spray collapse state of other fuel mixtures with different component proportions can also be predicted accurately.

<center>
    <img style="border-radius: 0.3125em;
    box-shadow: 0 2px 4px 0 rgba(34,36,38,.12),0 2px 10px 0 rgba(34,36,38,.08);" 
    src="ICEFpaper-5.png" alt="Image failed to load">
    <br>
    <div style="color:orange; border-bottom: 1px solid #d9d9d9;
    display: inline-block;
    color: #999;
    padding: 2px;">  Prediction result and mismatch analysis </div>
</center>

However, in Figure 9b, mismatches (circled by dash line) can still be found for the boundary cases between transition and non-collapse states. The reason could be the difference between non-collapse and transition states which is too small for the model to recognize. Subsequent improvements on prediction ability can be made by feeding this model with more data. The total prediction accuracy is over 95%. Through the feature evaluation and prediction processes of DTCs, a major finding is that the parameter $\left(K_1 / K_2\right) \cdot\left(P_a / P_b\right)$ is effective to describe the superheated degree of mixed fuels. This parameter can be used as an indicator for determining the spray collapse state of multi-component fuels.

## Extra Discussion: Initial Attempts of Reinforcement Learning from Human Feedback Models

Besides ResNet application, our ongoing work focuses on the potential of RLHF models, such as Visual-ChatGPT, to assist in spray image detection tasks. Visual ChatGPT is a model based on ChatGPT and a variety of visual foundation models (VFMs). It uses a Prompt Manager to bridge the gap between ChatGPT and VFMs. The user uploads an image and a language instruction. Then the Prompt Manager helps the model start a chain of execution of related VFMs. After a few iterations, Visual ChatGPT model can show the final result to address the user needs. Although the analysis on Visual ChatGPT’s performance has not been fully evaluated at this stage, some preliminary results demonstrate its promising potential in the spray image classification task. 

<center>
    <img style="border-radius: 0.3125em;
    box-shadow: 0 2px 4px 0 rgba(34,36,38,.12),0 2px 10px 0 rgba(34,36,38,.08);" 
    src="ICEFpaper-6.png" alt="Image failed to load">
    <br>
    <div style="color:orange; border-bottom: 1px solid #d9d9d9;
    display: inline-block;
    color: #999;
    padding: 2px;">  Initial attempts of using visual ChatGPT for image-based spray collapse state classification </div>
</center>

Since Visual ChatGPT has a language interface, the preliminary results are demonstrated using a dialogue case. Figure 10 shows the dialogue sample of Visual ChatGPT. This dialogue includes four rounds of Q1-A1: image input, Q2-A2: problem context, Q3-A3: refinement, and Q4-A4: validation. As depicted in Figure 10, the spray images are classified into Class A: collapse state, Class B: transition state, and Class C: non-collapse state. Firstly, the single-shot sample images of these three classes are given to the model. Secondly, a complex language instruction (problem definition) is entered and then this model can classify the unseen images based on the single-shot samples. Due to the limitations of current LLMs, it is computationally demanding to achieve fast prediction for large sample batches. Therefore, a dozen samples are used for accuracy test first. For single-shot training, the accuracy is 62.5% (10 correct labels over 16 samples). The wrongly classified images are similar to ResNet model. Spray state of Class B, which is under the transition state, is hard to be recognized since the edges of the six plumes are about to adhere to each other. Thus, a few-shot refinement is added to improve the model performance. Three more image samples of Class B and language instructions are given to the model. After refinement, the model finally improves the accuracy significantly to 91.7% (11 correct labels over 12 samples).


<center>
    <img style="border-radius: 0.3125em;
    box-shadow: 0 2px 4px 0 rgba(34,36,38,.12),0 2px 10px 0 rgba(34,36,38,.08);" 
    src="ICEFpaper-7.png" alt="Image failed to load">
    <br>
    <div style="color:orange; border-bottom: 1px solid #d9d9d9;
    display: inline-block;
    color: #999;
    padding: 2px;">  Success and challenges of visual ChatGPT for scientific image classification task </div>
</center>

Although the accuracy on large samples remains to be validated, two highlights for Visual ChatGPT can be found: First, much less labor for data labelling is required.  In other words, the Visual ChatGPT is a few-shot semi-supervised model which needs less training data. Second, the robust refinement capability from additional images and instructions is achieved. Specifically, Visual ChatGPT has higher flexibility for different downstream tasks with more input of language instructions. By this stage, the ResNet model still shows better accuracy and stability for spray collapse state detection. For now, this initial attempt of Visual ChatGPT demonstrates its promising potential in the field of spray image analysis. In our future work, this Visual ChatGPT model will be further analyzed with large data samples. New AI technologies such as RLHF models deserve to be noticed and explored for more possibilities in engine in-cylinder visualization research.



