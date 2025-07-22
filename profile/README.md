<!--

**Here are some ideas to get you started:**

🙋‍♀️ A short introduction - what is your organization all about?
🌈 Contribution guidelines - how can the community get involved?
👩‍💻 Useful resources - where can the community find your docs? Is there anything else the community should know?
🍿 Fun facts - what does your team eat for breakfast?
🧙 Remember, you can do mighty things with the power of [Markdown](https://docs.github.com/github/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax)
-->

## 🚀 프로젝트 개요

### **주제:** 산업군별 ESG 평가 지표에 따른 기업가치 분석

**팀 규모:** 4명  
**프로젝트 기간:** 25.07.21 - 25.09.11  

## 📋 Git 협업 규칙

### 🔸 커밋 메시지 규칙

```
<type>(<scope>): <subject>

[본문 - 선택사항]
[이슈번호 - 필요시]
```

**타입 분류:**

| type | 설명 | 예시 |
|------|------|------|
| **feat** | 새로운 기능 추가 | `feat(analysis): 데이터 전처리 함수 구현` |
| **fix** | 버그 수정 | `fix(viz): 그래프 렌더링 오류 해결` |
| **docs** | 문서 업데이트 | `docs: 분석 결과 해석 가이드 추가` |
| **refactor** | 코드 리팩토링 | `refactor(model): 예측 모델 성능 최적화` |
| **test** | 테스트 코드 | `test: 데이터 검증 테스트 케이스 추가` |
| **chore** | 기타 작업 | `chore: 라이브러리 의존성 업데이트` |

### 🔸 브랜치 네이밍 규칙

**기본 구조:** `브랜치 타입/설명-키워드`

| 브랜치 타입 | 용도 | 네이밍 예시 |
|------------|------|-------------|
| `feature/` | 새로운 기능 개발 | `feature/data-preprocessing` |
| `analysis/` | 데이터 분석 작업 | `analysis/customer-segmentation` |
| `viz/` | 시각화 구현 | `viz/dashboard-charts` |
| `docs/` | 문서화 작업 | `docs/analysis-report` |
| `hotfix/` | 긴급 수정 | `hotfix/critical-data-error` |

## 🔄 협업 프로세스

### **1단계: 이슈 생성**
- 작업 전 반드시 이슈 등록
- 담당자, 라벨, 마일스톤 설정
- 예상 소요시간 명시

### **2단계: 브랜치 생성 & 개발**
> 예시
```bash
git checkout -b feature/data-analysis
# 개발 작업 진행
git add . && git commit -m "feat(analysis): 고객 세분화 알고리즘 구현"
```

### **3단계: Pull Request**
- **최소 1명 이상**의 팀원 리뷰 필수
- PR 템플릿 활용하여 상세 설명 작성
- 관련 이슈 번호 연결 (`Closes #이슈번호`)

### **4단계: 코드 리뷰 & 머지**
- 리뷰어는 **24시간 내** 피드백 제공
- 승인 후 `main` 브랜치로 머지

## 📂 프로젝트 구조
> 예시 
```
📁 data-analysis-project/
├── 📁 data/              # 원시 데이터
├── 📁 notebooks/         # Jupyter 노트북
├── 📁 src/              # 소스 코드
├── 📁 reports/          # 분석 보고서
├── 📁 visualizations/   # 시각화 결과
└── 📄 README.md
```

## 👥 팀 커뮤니케이션

### **주간 스크럼** (매주 월요일 오전)
- 지난 주 진행사항 공유
- 이번 주 목표 설정
- 블로커 및 도움 요청 사항 논의

>스크럼:
스크럼은 반복적인 스프린트 주기를 가지며, 각 스프린트마다 목표를 설정하고 팀원들이 협력하여 달성합니다.

>블로커: 블로커는 스크럼 팀이 스프린트 목표를 달성하는 데 방해가 되는 요소들을 말합니다. 예를 들어, 특정 기술 문제, 필요한 자원 부족, 이해관계자와의 소통 문제 등이 블로커가 될 수 있습니다.


### **코드 리뷰 문화**
- 건설적이고 상세한 피드백 제공
- 코드 품질과 학습을 위한 상호 리뷰
- "Why?"에 대한 설명 중시

## 🛠️ 개발 환경

**공통 도구:**
- **언어**: Python 3.9+
- **분석**: Pandas, NumPy, Scikit-learn
- **시각화**: Matplotlib, Seaborn, Plotly
- **협업**: GitHub, Jupyter Notebook

**코드 품질 관리:**
- 코드 스타일: PEP8 준수
- 주석: 복잡한 로직에 반드시 설명 추가

## 📈 프로젝트 마일스톤

| 주차 | 목표 | 담당 |
|------|------|------|
| 1-2주 | 데이터 수집 & 전처리 | 전체 |
| 3-4주 | 탐색적 데이터 분석 | 분석팀 |
| 5-6주 | 모델링 & 예측 | 모델링팀 |
| 7-8주 | 시각화 & 최종 보고서 | 전체 |

## 🎯 성공 기준

- ✅ **협업 효율성**: PR 리뷰 24시간 내 완료율 90% 이상
- ✅ **코드 품질**: 주요 함수 90% 이상 문서화
- ✅ **프로젝트 완성도**: 분석-모델링-시각화-보고서 전 과정 완료
- ✅ **학습 목표**: 팀원 개별 기술 역량 향상

## 🔗 주요 링크
- 📝 **회의 기록**: [노션 회의록](https://www.notion.so/238965df706180a88062e0e933242759?v=238965df706180979b07000ce623e42e)
- 📚 **참고 자료**:

> **💡 규칙 업데이트 제안이 있다면 언제든 이슈로 등록해 주세요!**  
> **함께 성장하는 협업 문화를 만들어 갑시다 🚀**

