'f4' 컬럼 데이터에 'FJ'가 포함된 데이터 찾기
cond = df['f4'].str.contains('FJ')
df = df[cond]

