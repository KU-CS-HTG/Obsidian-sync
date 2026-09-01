pandas에서 날짜, 시간 데이터를 효과적으로 처리하기 위해 사용하는 자료형으로, 파이썬은 데이터를 불러올 때 날짜, 시간을 기본적으로 object(문자열)로 처리하기 때문에 날짜, 시간처럼 다루고 싶으면 자료형을 datetime으로 변경해줘야 한다 (parsing)
df = pd.read_csv("date_data.csv") 
df['Date2'] = pd.to_datetime(df['Date2'], format='%Y:%m:%d') 
df['Date3'] = pd.to_datetime(df['Date3'], format='%y/%m/%d') 
df['DateTime1'] = pd.to_datetime(df['DateTime1'], format='%y-%m-%d %H:%M:%S') df['DateTime2'] = pd.to_datetime(df['DateTime2'], format='%Y-%m-%d %H-%M-%S')
![[Pasted image 20260825171521.png]]
위의 2개는 format을 d까지만 적어서 날짜까지만 나오고, 아래 2개는 s까지 적어서 초까지 나오는 것 확인 가능
![[Pasted image 20260825171534.png]]
4개의 컬럼에만 parsing을 적용했기 때문에 Dtype도 4개만 datetime이고 나머지는 object이다

df['year'] = df['DateTime1'].dt.year
df['month'] = df['DateTime1'].dt.month
df['day'] = df['DateTime1'].dt.day
df['hour'] = df['DateTime1'].dt.hour
df['minute'] = df['DateTime1'].dt.minute
df['second'] = df['DateTime1'].dt.second
컬럼의 자료형이 datetime이면 이런 식으로 각 데이터에 접근할 수 있다

df['DateTime1'].dt.dayofweek
![[Pasted image 20260825171909.png]]
dayofweek으로 요일도 출력할 수 있다 (기본은 0이 월요일)


