결측치가 있는 데이터(행)을 모두 제거하고자 할 때,
df = df.dropna()로 간단하게 구현 가능
특정 column에 있는 결측치를 제거하고 싶을 때는 
df = df.dropna(subset=['f1']) 이렇게 해야 함