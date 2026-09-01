데이터프레임을 세부적으로 쪼개서 세로로 길게 만들어주는 함수
![[Pasted image 20260825114910.png]]
이런 데이터프레임이 있을 때,
pd.melt(df, id_vars=['Name']) 를 하면 Name열만 유지되고, 나머지는 Name을 기준으로 재편된다. (아래 데이터프레임 참조)
![[Pasted image 20260825115200.png]]
pd.melt(df, id_vars=['Name'], value_vars=['수학', '영어']) 를 하면 value_vars에 포함된 열만 변환된다.
![[Pasted image 20260825115442.png]]
