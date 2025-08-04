# 🌊 Seoul Wastewater Inflow Prediction using AI


  
  
  
  


## 🎯 프로젝트 개요  

**주제**  
기상·유동인구 기반 서울시 하수처리장 유입량 예측 AI 모델 개발

**목표**  
- 집중호우·도시 인구 변동으로 인한 하수 유입 급증을 사전 예측  
- 펌프·차단막·저류조 선제 운용으로 침수·오염·에너지 과소비 예방  
- 운영비 10–20% 절감, CSO(합류식 월류) 30% 이상 저감, 에너지 5–15% 절감  

**필요성**  
- 2017~2025.6, 8.5년간 축적된 기후 및 도시 인구 변동 분석  
- 합류식 하수관거 월류 문제 대응과 스마트시티 ESG 인프라 운영  

## 📊 데이터 및 기술 스택  

| 데이터 유형             | 출처                                   | 기간          |
|-----------------------|--------------------------------------|-------------|
| 하수처리량              | 서울 열린데이터광장 (OA-15561)          | 2017~2025.6 |
| 기상데이터(ASOS)        | 기상자료개방포털                         | 2017~2025.6 |
| 생활·유동인구           | 서울 열린데이터광장 (OA-14991, OA-15964) | 2017~2025.6 |
| 부가정보(요일·공휴일·계절) | 직접 생성                                 | N/A         |

**기술 스택**  
- Python 3.8+ · Jupyter Notebook  
- pandas · NumPy · Matplotlib · seaborn  
- scikit-learn · XGBoost · LightGBM · CatBoost  
- TensorFlow/Keras (GRU, TCN)  
- Streamlit · Plotly  

## 📂 프로젝트 구조  

```text
Seoul-Wastewater-Inflow-Prediction/
├── README.md
├── requirements.txt
├── .gitignore
├── data/
│   ├── raw/              # 원본 데이터
│   ├── processed/        # 전처리된 데이터
│   └── external/         # API 키, 참조 파일
├── notebooks/            # EDA 및 실험 노트북
│   ├── 01_data_collection.ipynb
│   ├── 02_preprocessing.ipynb
│   ├── 03_EDA.ipynb
│   └── 04_modeling.ipynb
├── src/
│   ├── data/             # 수집/전처리 코드
│   ├── models/           # 모델 학습 코드
│   └── visualization/    # 시각화 코드
├── models/               # 학습된 모델 파일
├── reports/              # 보고서, 그림, 발표자료
└── scripts/              # 실행 스크립트
```

## 🛠 설치 및 실행 방법  

1. 리포지토리 클론  
   ```bash
   git clone https://github.com/YOUNG-MONEY-TEAM/Seoul-Wastewater-Inflow-Prediction.git
   cd Seoul-Wastewater-Inflow-Prediction
   ```

2. 가상환경 생성 및 활성화  
   ```bash
   python -m venv venv
   source venv/bin/activate     # Windows: venv\Scripts\activate
   ```

3. 패키지 설치  
   ```bash
   pip install -r requirements.txt
   ```

4. 환경변수 설정  
   ```bash
   export SEOUL_API_KEY="your_seoul_key"
   export KMA_API_KEY="your_kma_key"
   ```

5. 데이터 수집  
   ```bash
   python scripts/collect_data.py
   ```

6. 모델 학습  
   ```bash
   python scripts/train_pipeline.py
   ```

7. 대시보드 실행  
   ```bash
   streamlit run src/visualization/dashboard.py
   ```

## 🔬 모델링 전략  

1. **회귀 모델**: XGBoost, LightGBM, CatBoost  
2. **시계열 모델**: GRU, TCN  
3. **앙상블**: Weighted Averaging + 룰 기반 보정  
4. **성능 지표**: MAE, RMSE, MAPE, R²  
5. **설명**: SHAP으로 변수 중요도 분석  

## 📈 주요 결과 예시  

| 모델     | MAE   | RMSE  | MAPE | R²   |
|----------|-------|-------|------|------|
| Ensemble | 1,247 | 1,892 | 2.3% | 0.91 |
| XGBoost  | 1,358 | 2,045 | 2.7% | 0.89 |
| GRU      | 1,425 | 2,156 | 2.9% | 0.87 |

## 📝 기여자  

| 역할        | 이름       | 이메일                             |
|------------|-----------|--------------------------------------|
| 팀장       | 윤하원     | dbsgk1102@gmail.com                |
| 팀원       | 이상욱     |                                    |
| 팀원       | 두소진     |                                    |
| 팀원       | 손형민     |                                    |

> **프로젝트 관련 문의**: dbsgk1102@gmail.com  
