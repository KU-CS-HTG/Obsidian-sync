[[datetime]]이 특정 시점의 날짜나 시간을 나타낸다면, timedelta는 두 시점 사이의 차이를 나타낸다. datetime 자료형을 빼거나 더하면 그 결과값은 timedelta 자료형이 된다.
day = pd.Timedelta(days=99) 
df['100day'] = df['DateTime4'] + day
![[Pasted image 20260826101537.png]]
99일 뒤 컬럼을 생성하는 코드는 위와 같고, timedelta 안에 hours, weeks, minutes, seconds 등이 다 들어갈 수 있다.
