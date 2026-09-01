print(df['DateTime1'].dt.to_period('Y'))
print(df['DateTime1'].dt.to_period('Q'))
print(df['DateTime1'].dt.to_period('M'))
print(df['DateTime1'].dt.to_period('D'))
print(df['DateTime1'].dt.to_period('H'))
to_period를 활용하면 각각 그 [[datetime]]이 어떤 연도, 분기, 월, 일, 시간 구간에 속해있는지도 알 수 있다
![[Pasted image 20260825172205.png]]
