# KT_Aivle_MINI3
# 📱 스마트폰 센서 기반 행동 인식 프로젝트

## 📝 프로젝트 개요
본 프로젝트는 **스마트폰 센서 데이터를 활용하여 사용자의 행동을 인식하는 AI 모델을 개발**하는 것을 목표로 합니다.  
센서 신호 데이터를 활용하여 **정적인 행동(앉기, 눕기 등)과 동적인 행동(걷기, 뛰기 등)을 분류**하고,  
이를 통해 **스마트 헬스케어, 운동 분석, 사용자 행동 예측 서비스에 활용할 수 있는 모델을 구축**합니다.  

### 🎯 **목표**
✅ 스마트폰 센서 데이터를 활용하여 **사용자의 활동을 분류**  
✅ 머신러닝/딥러닝 모델을 활용한 **행동 인식 모델 개발**  
✅ 행동 인식 데이터를 활용한 **실제 서비스 적용 가능성 검토**  

---

## 📂 데이터셋 소개

본 프로젝트에서는 **UCI Human Activity Recognition Dataset**을 활용합니다.  
📌 **데이터 출처:**  
🔗 [UCI Machine Learning Repository - Human Activity Recognition](https://archive.ics.uci.edu/ml/datasets/human+activity+recognition+using+smartphones)  

### 🔹 **데이터 특징**
| 데이터셋 | 샘플 개수 | 특징 |
|----------|----------|-----------------|
| train.csv | 7,352 | 훈련 데이터 |
| test.csv | 2,947 | 테스트 데이터 |

### 🔹 **주요 변수 설명**
| 컬럼명 | 설명 |
|--------|------|
| `tBodyAcc-mean()-X` | 몸의 가속도(X축) 평균값 |
| `tBodyAcc-mean()-Y` | 몸의 가속도(Y축) 평균값 |
| `tBodyAcc-mean()-Z` | 몸의 가속도(Z축) 평균값 |
| `tBodyAcc-std()-X` | 몸의 가속도(X축) 표준편차 |
| `tBodyAcc-std()-Y` | 몸의 가속도(Y축) 표준편차 |
| `Activity` | 행동 레이블 (6개 클래스) |

### 🔹 **행동 레이블 (Target)**
- `WALKING` (걷기)
- `WALKING_UPSTAIRS` (계단 오르기)
- `WALKING_DOWNSTAIRS` (계단 내리기)
- `SITTING` (앉기)
- `STANDING` (서 있기)
- `LAYING` (눕기)

---

## 🚀 프로젝트 수행 과정

### **1️⃣ 데이터 전처리**
- **결측치 처리 (Missing Value Handling)**
  - `dropna()`, `fillna()` 등의 기법을 활용하여 결측치 제거  
- **데이터 스케일링**
  - `StandardScaler()`를 활용한 정규화  
- **특징 선택 (Feature Selection)**
  - `Random Forest Feature Importance`를 활용하여 주요 변수 선택  

### **2️⃣ 행동 인식 모델 학습**
#### 📌 **머신러닝 모델**
- **Random Forest**
- **XGBoost**
- **LightGBM**

#### 📌 **딥러닝 모델**
- **LSTM 기반 시계열 분석 모델**
- **CNN 기반 신호 데이터 분류 모델**

### **3️⃣ 성능 평가**
- **Precision (정밀도), Recall (재현율), F1-score**  
- **Confusion Matrix 시각화**  
- **ROC Curve & AUC Score 분석**  

---

## 🛠 사용 기술

| 기술 | 설명 |
|------|------|
| **Python** | 데이터 전처리 및 모델 학습 |
| **TensorFlow / Keras** | 딥러닝 모델 학습 |
| **Scikit-Learn** | 머신러닝 모델 학습 |
| **Pandas / NumPy** | 데이터 처리 및 분석 |
| **Matplotlib / Seaborn** | 데이터 시각화 및 성능 분석 |

---

## 🔥 실행 방법

### 
```bash
1️⃣ 필수 라이브러리 설치
pip install -r requirements.txt
2️⃣ 데이터 전처리 및 모델 학습
python preprocess.py  # 데이터 전처리 실행
python train.py  # 모델 학습 실행
3️⃣ 모델 평가 및 테스트
python evaluate.py
```

## 📌 주요 개념 정리

### 🔹 **Human Activity Recognition (HAR)란?**
HAR은 **스마트폰, 웨어러블 센서 등을 활용하여 사용자의 행동 패턴을 자동으로 감지하는 기술**입니다.  
본 프로젝트에서는 **스마트폰 가속도계(Accelerometer) 및 자이로스코프(Gyroscope) 센서 데이터**를 활용하여  
사용자의 활동을 정밀하게 예측하는 모델을 구축합니다.  

---

### 🔹 **센서 데이터 개요**
| 센서 종류 | 설명 |
|----------|------|
| **Accelerometer (가속도 센서)** | 선형 가속도를 측정 (X, Y, Z축) |
| **Gyroscope (자이로스코프 센서)** | 회전 각속도를 측정 (X, Y, Z축) |

---

### 🔹 **모델 성능 평가 지표**
- **Precision (정밀도):** 모델이 행동을 예측한 것 중 실제 정답 비율  
- **Recall (재현율):** 실제 행동 중에서 모델이 올바르게 예측한 비율  
- **F1-score:** Precision과 Recall의 조화 평균  
- **ROC Curve & AUC:** 분류 모델의 성능을 평가하는 그래프  

---

## 🤝 기여 방법

1. 이 레포지토리를 **포크(Fork)** 합니다.  
2. 새로운 브랜치를 생성합니다. (`feature/새로운기능`)  
3. 변경 사항을 커밋합니다. (`git commit -m "추가된 기능 설명"`)  
4. 원격 저장소에 푸시합니다. (`git push origin feature/새로운기능`)



