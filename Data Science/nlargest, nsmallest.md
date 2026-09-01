가장 큰 몇 개, 가장 작은 몇 개를 찾을 때는 이걸 쓰는 게 제일 편하다
result = df['value'].nsmallest(25)
![[Pasted image 20260827155352.png]]
결과가 이렇게 인덱스로 나오기 때문에 보통 뒤에 sum이나 mean 같은 내장함수로 통계량을 도출해낸다
