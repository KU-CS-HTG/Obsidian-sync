데이터를 변경하거나 파생변수를 생성할 때 활용하는 함수
def cal(x): 
	if x >= 100: 
		return "No" 
	else: 
		return "Yes"
df['먹어도 될까요'] = df['칼로리'].apply(cal)
![[Pasted image 20260825114731.png]]
칼로리 컬럼을 활용하여 파생변수를 생성한 모습
