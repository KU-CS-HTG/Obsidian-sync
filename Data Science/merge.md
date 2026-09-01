[[concat]]에서 가로로 합칠 때 겹치는 column이 거슬리게 느껴지는데, 이 겹치는 column을 key(기준)으로 합치고 싶다면 merge를 활용하면 된다.
menu_info = pd.merge(price, cal, on='Menu')
![[Pasted image 20260826102426.png]]
이러면 menu 하나에 price, calories가 묶여서 합쳐지게 된다
