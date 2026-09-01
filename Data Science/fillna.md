**df['원산지'].fillna('코스타리카', inplace=True)** # 결측치 채우기
![[Pasted image 20260819155756.png]]

df = df.fillna(method='bfill')
bfill은 바로 아래값으로 결측치를 대체한다
df = df.fillna(method='ffill')
ffill은 바로 위 값으로 결측치를 대체한다


