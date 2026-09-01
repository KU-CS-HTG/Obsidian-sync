df['메뉴'].isin(['녹차']) # isin: 값이 있는지 확인
![[Pasted image 20260819155402.png]]

box = ['녹차', '카푸치노', '카페라떼']
cond = df['메뉴'].isin(box) # isin으로 여러 개의 값 한번에 찾기
df[cond] # 출력할 때는 cond가 행이기 때문에 앞에 df를 붙여야 함
![[Pasted image 20260819155458.png]]

**isin으로 조건을 만족하는 행 뽑아내기**
df_distance = df.groupby('user')['거리'].sum()
cond1 = df_distance >= 50
df_distance = df_distance[cond1]

filtered_data = df[df['user'].isin(df_distance.index)]
filtered_data
index를 활용하면 사용자별 거리 합이 50 이상인 행만 isin으로 확인할 수 있다
