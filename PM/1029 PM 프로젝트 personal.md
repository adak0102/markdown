# 10/29 PM 프로젝트 personal

### 데이터 가공 및 준비

##### 생산가능 인구 올려보기

>    	1. GIS 에서 수를 구/동 단위로 뽑아보기

##### 자전거도로 길이 구해보기

> 		1. 길이 구해서 필드에 저장
> 		2. 격자 중심점 위치 필드 더하기
> 		3. GIS에서 수를 구/동 단위로 뽑아보기
> 		> 데이터
> 		https://data-esrikrmkt.opendata.arcgis.com/datasets/%EC%84%9C%EC%9A%B8%EC%8B%9C-%EC%9E%90%EC%A0%84%EA%B1%B0%EB%8F%84%EB%A1%9C?geometry=126.468%2C37.376%2C127.508%2C37.757

> 	#안되면  디졸브 후에 합치는 것도 고민 해보기
> 	1. 격자별 도로 길이 tool-general-merge하고 (0)
> 	2. 한 테이블로 갖다붙인다 
> 	   격자 중심점 경위도 구한거 따로 셀 만들어서 그것도 격자별 도로 길이랑 Join
> 	   > 생산인구랑 join   > 격자 중심지 구한거랑 join 
> 	3. 격자 중심지별 도로 길이를 구할 수 있을라나?

##### 경사도 데이터 준비

> 	1. spatial join
> 	2. 그렇게 하면 100격자에 포인트가 여러 개 걸리니까 격자 당 값이 하나만 남게 될거야

##### 동별 join 데이터 준비

> 	1. 동별로 저 3가지 변수를 묶는거는 더 쉽겠지 다 spatial join해서 속성테이블 만들면

### 분석 방법 고민

> 	1. 위치 통일
> 	2. 어떤 목적함수?
> 	3. 알고리즘?

> ### 1. <u>파레토 최적함수</u> 스터디 필요
>
> ### 2. 3가지 도입가능지역 요소들 <u>정규화</u>해서 같은 지표로 비교하는 방법 고민
>
> ### 3. 3가지 도입가능지역 지표에 대해 <u>단순 합</u>일지, <u>십분위수</u>로 비교할 것인지, <u>10개의 단계에도 가중치</u>를 둘 것인지에 대한 고민 
>
> ### 4. <u>파이썬</u> 어떻게 사용할지 고민
>
> ### 	- API 경계 등 + 파이썬 내 GIS API 무언지 알아볼 것 
>
> 

## 파이썬 이용 고민

> 파이썬 내 gis API 알아보기

>  esri 사이트 참고

>  창호한테 물어보자 : api &  구, 동 별 경계 이용하는 법 



#### *참고 사이트 및 개념 정리*

> split 격자?
> -dissolve 격자?
> -길이재기?

>split 하는 거 격자 면으로
>
>http://www.biz-gis.com/index.php?mid=GISFAQ&document_srl=12254
>
>레이어를 격자 폴리곤으로 자르기 
>
>http://www.onspatial.com/2011/10/blog-post.html

>  [서울 생활인구 데이터를 격자 단위로 재할당하기](https://www.vw-lab.com/58) 
>
>  https://www.vw-lab.com/58   : 행정구역 점 뽑는거 가능할지도 ?
>


>  생활인구 데이터 
>
>  https://data.seoul.go.kr/dataVisual/seoul/seoulLivingPopulation.do





## 과정

> ## 자전거 도로 
>
> ​	**fishnet 만들어서 TID 셀 만듬 **
>
> - split 제대로 블로그 참조
>
>   http://www.biz-gis.com/index.php?mid=GISFAQ&document_srl=12254 이대로 했는데 오류 남, 제대로 쪼개지지 않음, 내가 절차중 실수한듯
>
>   http://www.onspatial.com/2011/10/blog-post.html 이거 참고해서 성공
>
> - split한거끼리 tool-general-merge처리해서 한번에 input 
>
> - fishnet과 spatial 조인해서 TID를 ID로 인식하도록 함
>
>   https://www.youtube.com/watch?v=OdhbbIEWPq0
>
> - 자전거 도로의 경우 link가 겹치는게 있어서 
>
> 1. ​	link기준 summarize->도로 length average
> 2.   ​    TID 기준 summarize->도로 length sum 처리 해줌
>
> **문제는 TID가 격자 이름과도 같은데 TID 기준 격자 중심 좌표가 구해지지 않음**
>
> http://www.biz-gis.com/index.php?mid=QnA&document_srl=56907
>
> 속성 테이블에서 새 셀 만든 후 geometry 분석의 x,y coordinate처리를 해줬을때 숫자가 이상하게 나와 오류가 생김

> ## DEM
>
> ascii로 csv를 못열어서 ArcToolbox에 있는 RastertoPoint이용
>
> https://www.youtube.com/watch?v=MZbgI2mEudU
>
> csv파일 만든 후에 fishnet과 spatial 조인 후 
>
> TID로 summarize , 고도 average처리함

> ## 생산인구
>
> fishnet과 격자 위치가 같음 
>
> fishet안만들고 여기다 TID줘도 됐을 것 같았음
>
> 여튼 얘는 그냥 join하면 되는데 찾아보기 귀찮아서 위에 하던데로 spatial 조인 후 ,
>
>  TID 기준으로 summarize, val average처리함
>
> >  생활인구 데이터로는 좌표가 나오지 않아 복잡한 처리가 필요한 것 같음
> >
> >  https://www.vw-lab.com/58





#### 파레토 최적함수

>  대중교통 취약성이랑 도입용이한 지역이라는 두가지 목적이 상이한 두 함수가 있는데,
> 상이한 목적에 얼만큼씩 각자의 조건을 만족시키면서 혹은 대중교통개선 혹은 도입이 적합한구역 중 어떤것에 더 비중을 높이면서 도입지를 선정할 것인지 그 비중을 선택할 수 있도록 가중치 함수를 만드는 방법



