
df.sort_index() # sort_index: 인덱스 순으로 정렬(아무것도 안쓰면 오름차순)
![[Pasted image 20260819152901.png]]
df 원본은 안 바뀌어서 df로 검증하면 안됨 - 원본에 반영하려면 inplace 활용

df.sort_index(ascending=False) # sort_index로 인덱스 기준 내림차순 정렬
![[Pasted image 20260819152928.png]]

df.sort_values('메뉴', ascending=False) # sort_values로 값 기준 정렬
![[Pasted image 20260819152954.png]]

df.sort_values(["가격", "메뉴"], ascending=[False, True], inplace=True) # 2개 이상의 기준 정렬
![[Pasted image 20260819153106.png]]

df.reset_index() # 정렬된 상태에서 인덱스 초기화
![[Pasted image 20260819153135.png]]
원래 인덱스인 index 컬럼이 새로 생기고, 얘는 보통 drop으로 지움

