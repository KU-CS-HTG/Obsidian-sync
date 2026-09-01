결측치가 있는 데이터만 선택하고 싶을 때 isnull 활용
cond = df['f1'].isnull()
df[cond]

df.isnull().sum() - 컬럼별로 결측치가 몇 개 있는지 세기

