# AIAP_Diabetes_Prediction_Model
: 이 프로젝트는 당뇨병 환자 데이터를 바탕으로 머신러닝 모델을 구축하고, 사용자가 입력한 신체 지표에 따라 당뇨 위험도를 실시간으로 예측해 주는 웹 인터페이스를 구현한 토탈 프로젝트입니다.

# Pipeline

📂 AIAP_Diabetes_Prediction_Model  
├── 📂 data/    
│   └── diabetes.csv                # 학습 및 테스트에 사용된 당뇨병 데이터셋  
├── 📂 notebooks/  
│   ├── AIAP_final1.ipynb           # 1단계: 데이터 전처리 및 탐색적 데이터 분석(EDA)  
│   ├── AIAP_final2.ipynb           # 2단계: 특성 공학(Feature Engineering) 및 기본 모델링  
│   ├── AIAP_final3.ipynb           # 3단계: 모델 튜닝 및 하이퍼파라미터 최적화  
│   └── AIAP_final4.ipynb           # 4단계: 비침습모델   
├── 📂 web/  
│   ├── index-dark.html             # 웹 구현 1 (모델3 웹 구현_스타일 다크모드 UI)  
│   └── index-light.html            # 웹 구현 2 (모델4 웹 구현_비침습 당뇨 예측 라이트모드 UI)  
└── 📄 README.md                    # 프로젝트 소개 및 설명 문서 (메인 화면)  


## ⚙️ 분석 및 모델링 프로세스 (Pipeline)

본 프로젝트는 총 4단계의 파이프라인으로 체계적으로 진행되었습니다.

1. **[1단계] 데이터 로드 및 EDA (`AIAP_final1.ipynb`)**
   - 데이터 분포 확인, 결측치 처리 및 기초 통계 분석 진행
2. **[2단계] 특성 공학 및 기본 모델링 (`AIAP_final2.ipynb`)**
   - 변수 스케일링, 파생 변수 생성 및 Baseline 모델 구축
3. **[3단계] 모델 튜닝 (`AIAP_final3.ipynb`)**
   - 다양한 알고리즘 비교 분석 및 하이퍼파라미터 최적화(GridSearchCV 등)
4. **[4단계] 최종 모델 평가 (`AIAP_final4.ipynb`)**
   - 혼동 행렬(Confusion Matrix), AUC-ROC 스코어 등을 통한 최종 모델 검증

---

## 🌐 웹 인터페이스 구현 (Web Interface)

Tailwind CSS와 JavaScript를 활용하여 사용자가 채혈 없이도 기본 신체 지표를 입력해 위험도를 확인할 수 있는 UI를 제작했습니다.

### 1️⃣ 토스 스타일 다크모드 UI (`web/index-dark.html`)
- 신뢰감을 주는 토스(Toss) 시그니처 블루 포인트를 활용한 다크모드 디자인
- 대사 비율 및 공복 혈당 관리 가이드 매칭 시스템 탑재

### 2️⃣ 비침습 당뇨 예측 라이트모드 UI (`web/index-light.html`)
- 깔끔하고 부드러운 화이트/핑크 톤의 대시보드 스타일
- 나이 대비 비만도(BMI) 가중치 분석을 통한 경계선 단계 세부 스위칭 가이드 제공

---

## 🛠️ 사용 기술 및 라이브러리 (Tech Stack)

- **Data Science**: Python, NumPy, Pandas, Scikit-learn, Matplotlib, Seaborn
- **Frontend**: HTML5, JavaScript (ES6+), Tailwind CSS (v4)
- **Environment**: Google Colab (T4 GPU Environment)
