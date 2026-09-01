reset_index: 꼭 [[groupby]]가  아니어도 함수를 적용한 이후 인덱스가 기존과 달라지는 경우가 많은데, 이럴 때 새로운 데이터프레임으로 재구성해주는 함수 (이거 안하면 groupby된 결과물에서 유의미한 결과를 도출해내지 못하는 경우가 많으니 groupby랑 세트라고 생각하기)
df.groupby(['원산지', '칼로리']).mean(numeric_only=True).reset_index()
![[Pasted image 20260825120423.png]]