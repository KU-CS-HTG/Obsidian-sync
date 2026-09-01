agg: 여러 개의 컬럼에 대해 다양한 집계 연산 동시에 수행 가능 
df.groupby(['원산지', '메뉴']).agg(['mean', 'sum'])
![[Pasted image 20260825120222.png]]



