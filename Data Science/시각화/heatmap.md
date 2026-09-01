2차원 배열로 된 데이터의 각 요소를 색상을 활용해 시각화하는 것
import seaborn as sns
import pandas as pd
df = pd.DataFrame({'+score':[5,4,3], '-score':[2,1,5]}, index = ['Python','R','SQL'])
sns.heatmap(df, annot=True, fmt = '.1f') - annot로 숫자 표시 여부 결정, fmt로 소수점 얼마나 표시할지 결정
![[Pasted image 20260828180331.png]]
