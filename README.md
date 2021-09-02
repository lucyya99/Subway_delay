# Subway_delay
## 프로젝트 개요
### 공공데이터를 활용하여 서울 교통공사 지하철 지연 시간 예측하기
* 사람들의 승하차 인원이 많아지면 지하철 지연이 발생할까?라는 궁금증에서 시작함
* 승하차 인원 외에 요소들도 크롤링 하여 알아볼 예정.
### 데이터 출처
* 서울교통공사 연도별 일별 시간대별 역별 승하차 인원
http://data.seoul.go.kr/dataList/OA-12921/F/1/datasetView.do
* 서울교통공사 간편지연증명서
http://www.seoulmetro.co.kr/kr/delayProofList.do?menuIdx=543

* 현재 간편지연증명서의 크롤링 가능 여부가 확인되지 않아, 확인 후 작업 내용을 올릴 예정.
* robots.txt에서는 가능하다고 적혀있지만, 홈페이지 내부에 복제가 안된다는 내용 확인.

## 데이터 프레임 만들기
### Subway_moving_dataframe
* 승하차 인원을 전부 합한 양 = 이동량이라고 정의.
* pandas, seaborn 등의 패키지를 활용하여 이동량을 시각화
### Subway_delay_dataframe
* 간편지연증명서의 내용을 크롤링하여, 지연 시간 파악.
* 크롤링 내용 중 결측치가 많아 지연되는 내용만 csv 파일에 저장.
