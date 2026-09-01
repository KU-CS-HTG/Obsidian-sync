[[groupby]] 이후 다중 인덱스가 설정된 상태에서 특정 인덱스를 컬럼으로 변환하는 기능
grouped = df.groupby(['커피종류', '컵크기'])['판매량'].sum()
![[Pasted image 20260825122428.png]]
여기서 컵크기를 컬럼으로 바꾸고 싶으면 (지금은 기준임) 
grouped.unstack() (기본값이 -1이라서 뒤에서 첫번째인 컵크기가 선택됨)
![[Pasted image 20260825122657.png]]
grouped.unstack(level=0) - 이러면 커피 종류를 컬럼으로 바꿀 수 있음
![[Pasted image 20260825122732.png]]
grouped.unstack().unstack() - 한번에 여러 번 적용할 수도 있음
![[Pasted image 20260825122912.png]]
