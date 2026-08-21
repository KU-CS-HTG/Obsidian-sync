df['메뉴'].isin(['녹차']) # isin: 값이 있는지 확인
![[Pasted image 20260819155402.png]]

box = ['녹차', '카푸치노', '카페라떼']
cond = df['메뉴'].isin(box) # isin으로 여러 개의 값 한번에 찾기
df[cond] # 출력할 때는 cond가 행이기 때문에 앞에 df를 붙여야 함
![[Pasted image 20260819155458.png]]