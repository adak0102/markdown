## 1103 MC PM project

행정동 shp 5174

좌표바꾸기

>  Define Projection (Data Management)



피벗

> field 열 선택-summarize기능(R의 groupby와 같음 )





- 알고리즘 공부

> apriori
>
> -12시/1시

> 각자 많이 나오는 거랑
>
> 대중교통이랑 조인했을때 많이 나오는 걸 보기
>
> c1 
>
> c2(two frequent item sets) c3 c4...
>
> -> join 
>
> [C2;D] c2 means all the frequent 2 items
>
> [L2] minimum support=2 
>
> [c3] 
>
> [L2]



> [ 연관 분석에서의 지지도와 신뢰도 ]
> A와 B상품의 지지도 = A상품과 B상품을 같이 구입한 횟수 / 전체 구매 횟수
> A상품에 대한 B상품의 신뢰도 = A상품과 B상품의 동시출현 횟수 / A상품의 출현 횟수
>
> 지지도는 "동시 출현 개수 / 전체 구매리스트"
> 신뢰도는 "동시 출현 개수 / 기준 상품 리스트" 
>
> 위의 식대로라면 지지도는 절대 신뢰도보다 높을 수 없으며 같거나 낮을 수 밖에 없는 수치이다.
>
>
> 지지도만으로도 일정 이상의 데이터만으로 연관성을 파악할 수 있으며, 특정 이상값의 신뢰도를 
> 추천한다는 경우에는 신뢰도까지 파악하여 처리하게 된다.
>
> 그리고 신뢰도는 association_rules()라는 함수로 구할 수 있어요...
> 점검해볼만한 소스를 준비해서 드릴께요.





> 동시구매표로 부터 간단한 규칙 (예: 사이다를 구입하는 고객은 오렌지 쥬스를 산다)을 만들 수 있다.
> 두 품목을 함께 산 경우는 총 5번의 구매 중 2번 일어났으며 사이다를 산 3번의 구매 중 오렌지 쥬스가 2번 구매되었다.
> 연관 규칙은 “If A, then B”와 같은 형식으로 표현된다.
> 모든 “if-then” 규칙이 유용한 규칙이 아니다.
> 찾아진 규칙이 유용하게 사용되기 위하여는
>
> - 두 품목 (품목 A와 품목 B) 이 함께 구매한 경우의 수가 일정 수준 이상 이여야 하며(일정 이상의 지지도)
>
> - 품목 A를 포함하는 거래 중 품목 B를 구입하는 경우의 수가 일정수준 이상 이여야 한다 (일정 이상의 신뢰도)
>
>   **[출처]** [연관분석(Assciation Rule)](https://blog.naver.com/dear_inwoo/110129191704)|**작성자** [인우기술](https://blog.naver.com/dear_inwoo)

> 단점, 
>
> 항목이 많아지면 어려움..,
>
> 

- 시각화 몇개 더 

>  표준화 값의 빈도분퍼
>
> -2시





- 접근성 분석 할 방법 찾기!!!!!!!-> GIS 사용 또는 목적함수
- 알고리즘 사용방법

