---
title: "Week1-3"
excerpt: "CP2 pytorch week1-3 assignment"

categories:
    - Blog
toc: true
toc_sticky: true

data: 2022-05-11
last_modified_at: 2022-05-11
---

NLG(Natural Language Generation)
===============================

언어를 생성
- 주어진 정보를 기반으로 축약, 보강, 재구성.
    - 축약 : 많은 데이터 중 핵심만 뽑는 것.
    - 보강 : 부족한 정보를 추가하는 것.
    - 재구성 : 기존 정보의 형태를 변형하는 것, 기존 정보로 추론해 답하는 것.

## NLG extractive summarization task

#### Text Abbreviation 
Summarization

- (참고) Abstractive Text Summarization : 원본 텍스트의 두드러진 아이디어를 포착하는 짧고 간결한 요약을 생성하는 작업이다. 생성된 요약에는 원본 텍스트에 나타나지 않을 수 있는 새 구문 및 문장이 포함될 수 있다.

#### 문제 정의
- Extractive Summarization : corpus input 내용에서 핵심만 뽑아내 요약문을 리턴하는 것.
    - extract는 원문에 있는 것을 그대로 뽑아 반환한다는 의미.
    - abstractive summarization 보다는 결과물이 제한적이지만 구현은 쉬울 수 있다.

#### 대표 데이터셋
CNN / Daily mail
- 300,000개의 CNN jounalist의 뉴스기사와 Daily mail이 들어있는 데이터셋이다.
- 각 article에 대한 summary와 highlight 문장으로 구성되어 있다. 
- 참고 : https://huggingface.co/datasets/viewer/?dataset=cnn_dailymail&config=3.0.0

#### task에 대한 SOTA 모델
1. HAHSum(Neural Extractive Summarization with Hierarchical Attentive Heterogeneous Graph Network)
    - 중복 인식 그래프로 문장 표현을 반복적으로 다듬고 메시지 전달을 통해 레이블 의존성을 전달한다.

2. MatchSum
    - 문장을 개별적으로 추출하고 문장 간의 관계를 모델링하는 일반적인 프레임워크를 따르는 대신, 추출 요약 작업을 의미 공간에서 소스 문서와 후보 요약을 (원문으로부터 추출) 일치시키는 의미 텍스트 일치 문제로 공식화한다. 특히, 의미 일치 프레임워크로의 이러한 패러다임 전환은 데이터 세트의 속성을 기반으로 한 문장 수준과 요약 수준 추출기 사이의 고유한 격차를 종합적으로 분석하는 데 근거가 있다.