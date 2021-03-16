# Module_Team_Project

1. 팀

김재원 진하영 정승철 한지혜


2. 팀 프로젝트 내용

# 데이터 소스
    1. 영화평점 데이터 or Box Office (주기적으로 변환하는 데이터를 가져오는 것이 목표)
        - https://www.imdb.com/chart.top

    2. 주식 (5분 or 15 분 ...)
        - https://finance.yahoo.com

    3. 날씨
        - https://openweathermap.opg/

    4. 암호 화폐
        - https://docs.poloniex.com/#introduction
        - https://poloniex.com/public?command=returnChartData&currencyPair=USDT_BTC&start=1414602755&end=9999999999&period=86400

        - timestamp to datetime
        - 날짜 최고가 최저가 시가 종가 거래량 평균가 등...

# 데이터 수집
    - 크롤링 (Crawling) Scrapy
    - Pipeline -> RDS(0)
    - Pipeline -> kafka(x) -> need to

# 데이터 저장
    - zookeeper + Kafka
    - kafka connect (source, sink)
    - kafka Broker...

# 데이터 분석 
    - Python data analysis (pandas, Numpy, Matplotlib)
    - 기본적인 기술 통계
    - 시각화...

# 시스템 운영
    - Public cloud
    - Docker container

데이터 소스 - 수집 - 저장 -처리 - 분석 - 표현

3. 구현 과정

    1. 주제 선정(배경)
    2. 기능 선정 - 3~5개 정도 ()

        - 코스피 200 ( ::: ... : ..:: .)
        - 당일(1주일, 1달) 가장 많이 오른(HOT 한) 종목 순위
        
        - 거래량 순위, 외국인 선호 주식 
        - 관련주(테마주) 추천
        
        - 재무재표 회사 신뢰도 등...
        
        - 종목 추천

        - 변동률 (최저 최고를 비교) -> 안정적인지 확인

    3. API 설계 - 입력 주소, 입력 파라미터, 출력 파라미터, 출력 데이터
        -  (GET) http://127.0.0.1:8000/movies/top
        -  (GET) http://127.0.0.1:8000/weathers/current

    4. Infrastructure 구성
    5. Scrapy 구현
    6. Kafka 구성
    7. RDS 구성
    8. Python + Django + RESTful API 구성
        - Djanggo(학습 전)
        - Rest framework(학습 전)
    9. 보고서 제출
    

1. 1개의 테이블 200개의 종목 넣어보기
    - 테이블이 존재하지 않으면 생성
    - 있다면 데이터 추가

    a) 이전 데이터 가져오기
    b) 실시간 데이터 가져오기

2. 재무제표 분석


