df.shape -> 출력: (7, 3) - (가로, 세로)

df.info() # column type 확인할 때 활용
![[Pasted image 20260819145645.png]]

df.corr(numeric_only=True) # 상관관계 파악 - 아래 결과는 가격과 칼로리는 0.7의 양의 상관관계를 갖는 것으로 해석 가능
![[Pasted image 20260819145848.png]]

df.describe() # 기술통계량 출력(수치형)
![[Pasted image 20260819150007.png]]

df_car.describe() # 기술통계량 출력(범주형)
![[Pasted image 20260819150045.png]]

