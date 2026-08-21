
df.replace('아메리카노', '룽고', inplace=True) # replace로 값 변경 
df.iloc[6,0] = "빙스커피" # ioc, iloc도 replace의 역할 수행 가능
![[Pasted image 20260819155857.png]]

change = {"룽고": "아메리카노", "녹차":"아이스티"}
df.replace(change, inplace=True) # 한번에 여러개 변경하려면 dictionary 활용 

