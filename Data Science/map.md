[[replace]]에 비해 유연성이 뛰어니, 딕셔너리나 사용자 정의 함수를 활용하여 보다 세밀하게 변환할 수 있는 함수
df = pd.DataFrame({'만족도': ['만족', '보통' ,'불만', '보통', '만족']}) 
mapping = {'만족': 3, '보통': 2, '불만': 1} 
df['만족도_숫자'] = df['만족도'].map(mapping)
![[Pasted image 20260825103120.png]]
결측치를 mapping할 때는 np.nan을 활용해야 한다 (import numpy as np도 없으면 위에 추가) (이때 'np.nan'이 아니라 그냥 np.nan이라는 것도 주의)