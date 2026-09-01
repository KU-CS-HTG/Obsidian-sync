[[bar]]와 유사한데, bar는 막대그래프라서 주로 범주형 데이터를 다룰 때 활용하고, hist는 히스토그램이라서 주로 연속형 데이터를 다룰 때 활용 (막대 사이 거리가 없음)
from matplotlib import pyplot as plt
x = np.random.normal(10,3,200)
plt.hist(x,bins=20) - 막대기 개수 조절 가능
![[Pasted image 20260828180011.png]]