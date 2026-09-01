데이터 타입이 정수인 column들만 확인하고 싶다면
cols = df.select_dtypes('int').columns
df[cols]
데이터 타입미 문자가 아닌 column들만 확인하고 싶다면
cols = df.select_dtypes(exclude='object').columns
df[cols]