# 🌊 Seoul Wastewater Processing Volume Prediction using AI

<div align="center"> <img src="https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=Python&logoColor=white"/> <img src="https://img.shields.io/badge/TensorFlow-FF6F00?style=flat-square&logo=TensorFlow&logoColor=white"/> <img src="https://img.shields.io/badge/scikit--learn-F7931E?style=flat-square&logo=scikit-learn&logoColor=white"/> <img src="https://img.shields.io/badge/Pandas-150458?style=flat-square&logo=pandas&logoColor=white"/> </div>

## 🎯 프로젝트 개요  

**주제**  
기상·유동인구 기반 서울시 하수처리장 **처리량** 예측 AI 모델 개발

**목표**  
- 집중호우·인구 변동에 따른 하수처리량 변동을 사전 예측  
- 선제적 시설 운용으로 효율 향상 및 비용 절감  
- 운영비 10–20% 절감, CSO 30% 이상 저감, 에너지 5–15% 절감  

## 📂 프로젝트 구조  

```
Seoul-Wastewater-Processing-Prediction/
├── README.md                # 프로젝트 개요·설치법·구조 안내
├── requirements.txt         # 필요한 Python 패키지 목록
├── .gitignore               # Git 추적 제외 대상
├── data/                    # 데이터 관련
│   ├── raw/                 # 원본 다운로드 데이터
│   ├── processed/           # 전처리 완료 데이터
│   └── external/            # 외부 참조 파일·API 키
├── notebooks/               # 분석용 Jupyter 노트북
│   ├── 01_data_collection.ipynb   # 데이터 수집 로직 실험
│   ├── 02_preprocessing.ipynb     # 전처리 및 결측치 처리
│   ├── 03_EDA.ipynb                # 탐색적 데이터 분석
│   └── 04_modeling.ipynb           # 모델링 실험
├── src/                     # 소스 코드
│   ├── data/                # 수집·전처리 모듈
│   ├── models/              # 모델 정의 및 학습 스크립트
│   └── visualization/       # 시각화·대시보드 코드
├── models/                  # 학습된 모델 파일(.pkl, .h5)
├── reports/                 # 리포트 및 발표 자료
└── scripts/                 # 배치 실행용 스크립트
```

## 🔬 모델링 전략  

- **회귀 모델**: XGBoost, LightGBM, CatBoost  
- **시계열 모델**: GRU, TCN  
- **앙상블**: Weighted Averaging + 룰 기반 보정  
- **설명**: SHAP으로 변수 중요도 분석  
- **평가지표**: MAE, RMSE, MAPE, R²  

## 🔀 브랜치 전략 (Git Flow 변형)  

```
main            # 운영 배포용 안정 브랜치 (PR 병합만)
develop         # 다음 배포 준비 브랜치
feature/123-add-gru-model    # 기능 개발 브랜치 (이슈 번호-간단설명)
release/v1.0.0               # 배포 전 최종 검증 브랜치
hotfix/v1.0.1-fix-bug        # 긴급 버그 수정 브랜치
```

- `feature/*` → 기능 단위로 `develop`에 PR  
- `release/*` → 배포 준비 후 `main`·`develop`에 병합  
- `hotfix/*` → 운영 버그 수정 후 `main`·`develop`에 병합

## ✍️ 커밋 메시지 규칙 (Conventional Commits)  

```
<type>(<scope>): <subject>

<body>

<footer>
```

- **type**  
  - feat: 새로운 기능  
  - fix: 버그 수정  
  - docs: 문서 변경  
  - style: 코드 포맷·문법 수정  
  - refactor: 리팩토링  
  - test: 테스트 코드  
  - chore: 빌드·설정 등
- **scope**: 변경 대상(예: data, model, api, docs)  
- **subject**: 한 줄 요약 (50자 이내, 소문자 시작)  

### 예시
```
feat(model): add GRU-based predictor

과거 LSTM 대비 학습 속도 30% 개선한 GRU 모델 추가

Closes #45
```

```
fix(data): handle missing population values

결측치를 중앙값으로 대체하도록 로직 수정하여 EDA 오류 해결

Closes #52
```

## 👥 팀 소개  

- **팀장**: 윤하원  
- **팀원**: 이상욱, 두소진, 손형민  

> **문의**: dbsgk1102@gmail.com  
