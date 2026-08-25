# 데이터프레임 csv 파일로 저장하기
df.to_csv('temp.csv')
![[Pasted image 20260819113001.png]]
데이터프레임을 그냥 to_csv로 바꾸면 쓸데없는 인덱스 열이 생김
df.to_csv('cafe.csv', index=False) # index=False면 index를 제외하고 저장
그래서 보통 위와 같은 방식을 많이 쓴다
# csv 파일 df로 불러오기
temp_df = pd.read_csv('temp.csv')
temp_df

