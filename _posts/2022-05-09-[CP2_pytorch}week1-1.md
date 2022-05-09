---
title: "Week1-1"
excerpt: "CP2 pytorch week1-1 assignment"

categories:
    - Blog
toc: true
toc_sticky: true

data: 2022-05-09
last_modified_at: 2022-05-09
---

## 1. 본인이 본 강의를 수강하는 목적에 대해서 자유롭게 적어보세요.

 우선 순위로 둔 프로젝트도 아니고 딥러닝 분야는 개인적으로 너무 어렵지만, 감정 분석이나 덱스트 분류는 평소 관심이 있던 내용이다.

## 2. Paperswithcode(https://paperswithcode.com/area/natural-language-processing)에서 NLP sub task 중에 2개를 선택하여 본인 블로그에 정리해보세요. task 별로 아래 3가지 항목에 대해서 정리하세요. (각 항목 고려 사항 참고)

### 1. Sentiment Analysis
    - 문제 정의
        - 텍스트의 긍정, 부정 또는 중립으로 분류하는 것.

    - 데이터 소개(대표적인 데이터 1개)
        - IMDB movie reviews
        - 긍정 또는 부정으로 레이블이 지정된 50,000개의 리뷰로 구성된 이진 감성 분석 데이터셋이다. 짝수 개의 긍정 및 부정 리뷰가 포함되어있다. 부정평가는 10점 만점에 4점, 긍정평가는 10점 만점에 7점을 받는다. 영화 한 편당 30개 이상의 리뷰가 포함되어 있지 않다. 레이블이 없는 데이터가 포함되어 있다.

    - SOTA 모델 소개(대표적인 모델 1개)
        - NB-weighted-BON + dv-cosine
        - 벡터 데이터에 대해 내적 대신 cosine similarity 사용 시 정확도가 향상하는 점에서 Naive bayes weighted bag of n-gram vector를 조합한 모델.

### 2. Text Classification
    - 문제 정의
        - 문장이나 문서를 적절한 카테고리로 지정하는 작업. 데이터셋에 따라 주제나 범주가 다양하다.
        - 감정 분류, 뉴스 분류, 인용 의도 분류 등이 포함된다.

    - 데이터 소개(대표적인 데이터 1개)
        - AG's News Corpus 
        - AG's Corpus의 4대 클래스 “World”, “Sports”, “Business”, “Sci/Tech” 주제의 기사 제목과 설명으로 구성된 데이터베이스 셋이다. 클래스 당 30,000개의 training sample과 1,900개의 test sample이 있다.

     - SOTA 모델 소개(대표적인 모델 1개)
        - XLNet
        - bidirectional information, Context dependency

## 3. 팀원들의 게시글을 읽고 피드백 댓글을 달아보세요.