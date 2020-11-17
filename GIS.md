## GIS

## 좌표계 맞추기

WGS84 -> 4326

신GRS80 -> 5174

> 서울과 서울의 대도시권 *시가화면*적은 용도지역 중 주거지역, 상업지역, 공업지역 *면적*의 합. 으로 산출

> Define Projection(Data management)

> https://www.osgeo.kr/17

> http://www.biz-gis.com/index.php?mid=pds&document_srl=66085

> https://www.seenbuy.kr/%ED%86%B5%EA%B3%84%EC%A7%80%EB%A6%AC%EC%A0%95%EB%B3%B4%EC%84%9C%EB%B9%84%EC%8A%A4-wgs84%EC%A2%8C%ED%91%9C-utmk-%EB%B3%80%ED%99%98-%EB%82%98%EC%9D%98%ED%86%B5%EA%B3%84%EC%A7%80%EB%8F%84/#sthash.Me6KVb1S.nxDvEJ3Y.dpbs

## 레이어 한글 속성데이터 깨짐

utf-8 /euc-kr

Q에서 레이어 설정->인코딩 잡음



QGIS에서 Shapefile 다른 이름으로 저장 하면서 인코딩을 UTF-8로 바꿔서 저장

## 행정동 데이터

(센서스경계)행정동경계 - 오픈마켓 - http://data.nsdi.go.kr/dataset/20171206ds00001

서울만 뽑아내기 : 숫자 코드 11로 시작하는 것 

## arc basemap

QGIS 이용

상단에 레이어 추가 버튼 옆에 있는 작은 삼각형 누르면 Add basemap 

지오레퍼런싱

## merge

Tool에 있는 merge에서 자료들 바로 Input해서 merge

### 경위도 좌표

Calculate Geometry에서 단위를 decimal degree로 고르면 경위도 좌표

밑에 유닛을 Decimal Degree

## 추가 사항

* gis 네트워크 분석

* 최적 경로나 최단 거리에 따른 시설 배치/자원 배분 직선거리가 아니라 도로망 따라서

GIS네트워크분석은 도로망 따라가는게 메인

도로망 따라가서 나오는 거리나 데이터로 입지배분 모형 적용가능

도로 노선별 속도 변수를 잡아주면 시간으로 환산 가능

- GIS 교차분석

  Intersect

  도형(도상)정보에 대한 중첩연산