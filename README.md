# hanbat_competition
한밭대학교 빅데이터 경진대회/💰대전광역시 유성구 MZ세대의 소비 규모 분석
(2022년 9월 ~ 2022년 11월)

👥**팀 구성**: 3인팀  
👩‍💻**역할**: 데이터 전처리 및 분석 알고리즘 활용(머신러닝)  
🧰**stacks**: ```python``` ```sklearn``` ```matplot``` ```seaborn``` ```pichart``` ```QGIS``` 

## 기획 의도
* 2021년 기준 유성구 내 MZ세대 비율은 같은 해 전국 MZ세대 비율보다 높음  
* 유성구 지역적 특성에 따른 소비 경향과 원인을 분석해 지역 경제 활성화 방향을 제시하고자 함  

## 분석 과정
### 데이터 수집
* 통계청(KOSIS, SGIS, MDIS), 공공데이터 포털을 통해 데이터 수집
* 세대당인구, 가구소득 300만원 미만, 가구소득 300~600만원 미만, Z세대사업체수비율, Z세대종사자수비율, 사업체신규비율 등  
<div align="center"><img src="https://github.com/noachilles/hanbat_competition/blob/main/assets/fig1.png"></div>  
<div align="center">fig 1. 각 지역별 분류한 MZ세대 인구비율</div>
<div align="center"><img src="https://github.com/noachilles/hanbat_competition/blob/main/assets/fig2.png"></div>
<div align="center">fig 2. 활용 데이터 목록</div>
### 데이터 전처리
* '가구주 연령별 가구당 월평균 가계 지출' 데이터와 유성구 MZ세대 인구 비율간 연산을 통해 MZ세대 평균 소비금액 산출  
* 법정동 코드 목록을 기준으로 행정동 기준 구분된 데이터를 Mapping  

### 데이터 분석  
* 각 변수에 대한 correlation 값을 추출하고 분석해 그래프로 제작함  
* 후진소거법을 사용해 교차 검증을 거쳐 학습에 활용할 attribute를 결정함  
<div align="center"><img src="https://github.com/noachilles/hanbat_competition/blob/main/assets/fig3.png"></div>
<div align="center">fig 3. correlation matrix</div>

### 분석 결과 시각화 
* QGIS 지도를 사용해 법정동 단위로 1인당 평균 소비 금액과 MZ세대 평균 소비 금액 분포를 지도상에 표시    
<div align="center"><img src="https://github.com/noachilles/hanbat_competition/blob/main/assets/fig4.png" width=30%/></div>
<div align="center"><img src="https://github.com/noachilles/hanbat_competition/blob/main/assets/fig5.png" width=30%/></div>
<div align="center">fig 4. 좌: 대전 내 법정동별 1인당 평균 소비 금액, 우: 대전 내 법정동별 MZ세대 평균 소비 금액</div>

* Pi-chart로 지역 간 소비 및 소득 분포를 도식화하고 특성을 비교  
<div align="center"><img src="https://github.com/noachilles/hanbat_competition/blob/main/assets/git6.png" width=80%/></div>
<div align="center">fig 5. Pi-chart 기준</div>

## 분석 결과 및 요약
* 법정동 단위 간 비교를 통해 MZ세대의 소비 경향에 가장 큰 영향을 끼치는 요인을 분석해 정리한 결과, 생활옇 주택수의 규모가 가장 큰 영향을 끼치는 것으로 드러남  
**따라서** 1인 ~ 2인 가구의 생활 인프라 구축을 제안  
<div align="center"><img src="https://github.com/noachilles/hanbat_competition/blob/main/assets/fig7.png" width=80%/></div>
<div align="center">fig 6. 분석 결과 시각화</div>
