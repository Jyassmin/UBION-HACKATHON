<<<<<<< HEAD
# 뱅뱅뱅 **'신용카드 연체기간 예측 및 연체고객경향 분석’**

🏆 2022 UBION Hackathon

<img width="1436" alt="1" src="https://user-images.githubusercontent.com/88031549/200560973-024f8bcc-8c95-4985-a88f-e6a05aaa9b7c.png">


<img width="1369" alt="2" src="https://user-images.githubusercontent.com/88031549/200561065-a97f3902-ee92-4857-bd6b-a7e91328e25d.png">


# **프로젝트 소개**

본 프로젝트는 카드사 고객을 대상으로 한국 신용카드 연체기준(NICE)에 근거한 연체기간을  예측하고, 연체고객에게 영향을 많이 미치는 주요 요인들을 중점으로 장단기연체자별 고객의 경향을 분석한다. 이를 통해 채무상환능력이 악회될 고객을 사전에 파악하고 연체고객의 경향에 따라 고객을 관리하여 카드사의 수익성을 높이는데 기여한다.

[ 배경 ]

최근 금리 인상 및 경기하락 추세가 이어지며 이자율, 물가가 상승해 국민들의 경제력이 하락하고 있는 실정이다. 이에 따라 카드사 고객은 낮아진 경제력으로 인해 카드 상환에 어려움을 겪으며 카드사 입장에서는 악성채권이 발생하고 있다. 2022년 상반기 말 기준 카드사 고정이하여신 중 추정손실 채권 평균 비중이 36.2%를 기록하며 채무상환능력이 악화된 고객들로 인해 카드사 수익성에 부정적인 영향을 미치고 있다.

[ 연체기간 예측 ]

 NICE에서 정의한 한국 신용카드 연체기간에 따라 고객을 4개의 클래스(0:비연체자, 1:단기연체자, 2:장기연체자, 3:초장기연체자)분류하고 고객의 부채, 상환, 신용, 개인 정보를 바탕으로 연체기간을 예측하는 연체기간예측모형 개발한다. 이에 따라 사전에 연체를 예측함으로써 채무상환능력이 악화될 고객들을 파악 및 관리하여 수익성에 기여할 수 있다.

[ 연체고객 경향분석 ]

 NICE에서 제시하는 국내 CB사 신용평가 요소(상환이력, 부채수준, 신용거래기간, 신용형태)에 근거하여 연체고객에게 영향을 많이 미치는 주요 피쳐(체불횟수, 체불액, 신용거래기간, 계좌수, 최소금액 지불여부 등)를 선정한다. 직관적인 분석을 위해 한국 신용카드 연체 기준에서 신용하락을 기준으로 고객을 단기연체자(class0), 장기연체자(class1)로 구분하였고, 위에서 선정한 주요 피쳐를 바탕으로 장단기 연체자별 경향을 분석하였다.(*ppt참고)

---

# **구조**

## **1. Preprocessing**

## 2. Feature Selection

- **Feature Importance(randomforest)**
- **Heat Map(corr)**
- **VIF**

## 3. 종속변수 다중클래스화

- 0 : 비연체자( 연체기간 ≤0
- 1 : 단기연체자(0일 < 연체기간 < 5일)
- 2 : 장기연체자(5일 ≤ 연체기간 < 30일)
- 3 : 장기연체자(30일 ≤ 연체기간)

(*NICE, 한국 신용카드 연체 기준에 따라)

## 4. Before Modeling

### 4-1. Scaling

- Minmaxscaling

### 4-2. Data Split

- Train set : Test set = 8 : 2

### 4-3. Oversampling

- SMOTE

## 5. Modeling & Evaluation

### 5-**1. Model**

- **RandomforestClassifier(최종모델)**
- LogisticRegression
- XGBClassifier
- DecisionTreeClassifier
- KNeiborsClassifier

### 5-2. Grid search

### 5-3. Evaluation(Test set)

- AUC : 0.94
- ACC : 0.9
- F1 Score : 0.75
- Recall : 0.73
- Precision : 0.9

(*카드 특성상 어느정도 연체가 되어야 수익이 발생하기 때문에 확실히 연체할 것 같은 고객들을 예측해서 관리할 수 있도록 Recall보다 Precision이 높은 모델을 사용)

## 6. 연체고객 경향분석

국내 CB사 신용평가 요소에 근거, 연체고객에 영향이 높은 주요피쳐 선정

한국 신용카드 연체기준의 신용하락유무에 따라 고객을 단기연체자, 장기연체자로 구분

- 신용거래기간에 따른 체불액 경향
- 나이에 따른 체불횟수 경향
- 나이에 따른 체불액 경향
- 이외 주요변수간 (반)비례관계 확인

(*아래 예시)

<img width="1018" alt="3" src="https://user-images.githubusercontent.com/88031549/200561113-03f653cc-394e-4f5e-926d-c675d06b26a0.png">

<img width="1019" alt="4" src="https://user-images.githubusercontent.com/88031549/200561138-21d90538-3b38-430a-ad40-58fc8cb066c9.png">
=======
# UBION-HACKATHON
UBION - 해커톤 / 22.10.18 ~ 22.10.31
>>>>>>> 44f5680c739676c434d55b96e30a3db260a66239
