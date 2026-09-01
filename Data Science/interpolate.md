보간법에 활용되는 함수
보간법: 이미 알고 있는 데이터 점들을 바탕으로 비어 있는 부분을 추정하는 것
df_sp2['cylinders'] = df_sp2['cylinders'].interpolate(method='linear')
이렇게 쓰면 비어 있는 부분을 선형으로 추정하게 된다.

