카테고리별 개수를 확인하기 위한 함수
df['subscribed'].value_counts()
![[Pasted image 20260826151701.png]]
df['subscribed'].value_counts()[0] 이라고 쓰면 16에 접근할 수 있다
날짜에 접근하고 싶다면 index를 활용해야 하는데, 한 줄로 쓰면 코드의 직관성이 떨어지기 때문에 
df_vc = df['subscribed'].value_counts()
df_vc.index[0] 
이렇게 두 줄로 표현하면 된다