---
title: "Week1-2"
excerpt: "CP2 pytorch week1-2 assignment"

categories:
    - Blog
toc: true
toc_sticky: true

data: 2022-05-10
last_modified_at: 2022-05-10
---

NLU 
==========

##
NLU(Natural Language Understanding)

언어를 "이해"하는 것

- Syntacic(문법적으로 맞는지 판단) 

- Semantic(문장의 의미를 파악)
    -의미 : 감정 분석(긍정/부정), 문장간 유사도, 의도 파악, 질문에 대답, 추론 등


프로그램이 문법과 문장의 의미를 잘 이해하고 있는 것.

## NLP sub task

#### Sentiment Analysis
- 문제 정의
    - text의 감성의 극성(긍정/부정)을 분류
    - 이진분류(긍정/부정) 또는 이진분류에 중립 포함(긍정/중립/부정)된 분류
    - 예시 : 상품 & 서비스 리뷰 데이터 긍정/부정 판별


- DataSet : GLUE
    - GLUE(General Language Understanding Evaluation benchmark)는 단일 언어 작업 CoLA 및 SST-2, 유사성 및 패러프레이징 작업 MRPC, STS-B 및 QQP, 자연어 추론 작업 MNLI, QNLI, RTE 및 WNLI를 포함한 9가지 자연어 이해 작업의 모음이다.

- SOTA model
    - SMART-RoBERTa Large

    - 1. Smoothness-inducing regularization, which effectively manages the capacity of the model. 
    - 2. Bregman proximal point optimization, which is a class of trust-region methods and can prevent knowledge forgetting. 


##### 참고 링크
- https://paperswithcode.com/dataset/glue
- https://paperswithcode.com/sota/sentiment-analysis-on-sst-2-binary
- https://hryang06.github.io/nlp/NLP/