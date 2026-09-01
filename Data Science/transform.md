같은 컬럼이어도 특정 기준에 맞는 통계량을 구하고 싶을 때는 [[groupby]]를 쓸 때 transform함수를 활용해줘야 한다.
![[Pasted image 20260825121148.png]]
price = df.groupby('과일')['가격'].transform("mean")
![[Pasted image 20260825121209.png]]
price 배열 자체는 순수하게 평균만 여러 번 적혀 있기 때문에 transform은 시각화 용도로 사용한다기보다는 이를 활용해 결측치를 채우는 식으로 주로 활용
df['가격'] = df['가격'].fillna(price)
![[Pasted image 20260825121335.png]]'

**주의점**
df['가격'] = df.groupby('과일')['가격'].transform("mean") 처럼 한 큐에 해버리려고 하면 결측치만 채워지는 게 아니라 기존 값들이 싹 다 평균으로 바뀐다는 문제가 있음
