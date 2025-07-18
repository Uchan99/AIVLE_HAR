# 📱 Human Activity Recognition (HAR) - 2단계 행동 분류 모델링

> 스마트폰 센서 데이터를 활용한 정적/동적 행동 분류 및 세부 행동 인식

---

## 🗓️ 프로젝트 기간
2025.04.14 ~ 2025.04.15

## 👥 팀 구성
- 팀원: 6명
- 내 역할: **팀장 (모델링 및 전체 코드 구현 총괄)**

---

## 📌 프로젝트 개요

본 프로젝트는 UCI HAR Dataset의 원시 데이터를 활용하여 **2단계 행동 분류 모델 파이프라인**을 설계하고 다양한 딥러닝 모델을 실험하여 최적의 분류 성능을 도출하는 데 목적이 있습니다.  
특히, 정적 vs 동적 행동 분류 (1단계)와 세부 행동 분류 (2단계)로 나누어 **계층적 분류 전략**을 적용하였습니다.

---

## 📂 사용 데이터셋

- **UCI HAR Dataset**  
  [Human Activity Recognition Using Smartphones](https://archive.ics.uci.edu/ml/datasets/human+activity+recognition+using+smartphones)

---

## 🛠 사용 기술

- Python, Pandas, NumPy  
- PyTorch  
- Scikit-learn  
- Jupyter Notebook

---

## ⚙️ 주요 전처리

- 불필요한 센서 컬럼 제거
- Sensor data normalization (정규화)
- 활동 레이블을 **정적 / 동적**으로 이진화하여 1단계 라벨 생성
- 원-핫 인코딩 및 타깃 변환 처리

---

## 🧠 모델링 전략

### 📍 1단계 모델: 정적 vs 동적 행동 분류
- 입력: 정규화된 센서 시계열
- 모델 구조: Fully Connected Neural Network (Baseline / 확장 모델 / 튜닝 모델 등 비교)
- 목표: 정적(0) vs 동적(1) 이진 분류

### 📍 2단계 모델: 세부 행동 분류
- 입력: 1단계에서 분류된 클래스별로 분리
- 정적 행동: Sitting / Standing / Laying 분류
- 동적 행동: Walking / Upstairs / Downstairs 분류
- 각각 별도의 모델로 학습 및 평가

---

## 📈 성능 결과

- 전체 모델 정확도: **93% 이상**
- 단순한 모델에서도 높은 성능 → 전처리 품질의 중요성 확인
- 세부 클래스 간 **오분류 분석을 통한 개선점 도출**

---

## 🧩 프로젝트 확장 및 후속 실험
https://github.com/Uchan99/AIVLE_HAR

프로젝트 이후, UCI HAR Dataset의 **집계 버전 데이터를 활용한 실험**을 별도 팀 프로젝트로 진행하였습니다.  
- 간결한 구조의 모델을 사용하되, **전처리~모델링~예측~결과 저장까지 자동화**
- 데이터 구조가 달라져도 적용 가능한 **범용 파이프라인 설계** 실험
- **실제 운영 환경에서의 활용성 고려**한 구조 설계 경험 확보

---

## 🧠 회고 및 인사이트

- **다단계 분류 전략**의 유효성 체감 (특히 유사 클래스 구분에 효과적)
- 전처리가 잘 된 데이터에서는 **복잡한 모델보다 단순한 모델이 더 잘 작동할 수 있음**
- 팀장으로서 프로젝트 리딩, 실험 설계, 코드 리뷰 및 통합 경험 수행

---

## 📁 폴더 구조

```bash
📦 HAR-2Stage-Classifier/
├── 1. EDA 및 전처리.ipynb
├── 2. 기본 모델링.ipynb
├── 3. 단계별 모델링.ipynb
├── AI 미프1차_03조_최종.pptx
├── README.md
└── requirements.txt (필요시)
```
