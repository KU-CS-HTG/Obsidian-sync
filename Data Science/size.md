[[groupby]]에서 기준별 개수를 집계하고 싶다면 [[value_counts]]가 아니라 size를 활용해야 한다
df['주문연월'] = df['주문시간'].dt.to_period('M')
df.groupby('주문연월').size() - 주문연월별 주문 개수
![[Pasted image 20260827145728.png]]
