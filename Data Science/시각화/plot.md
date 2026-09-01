선으로 된 그래프를 그릴 때 활용
from matplotlib import pyplot as plt
plt.figure(figsize=(15,10))
plt.plot([1,2,3],[4,5,6], label= 'x1')
plt.plot([1,2,3],[6,5,4], label= 'x2')
plt.legend()
![[Pasted image 20260828170741.png]]
파라미터는 꼭 위의 형태가 아니어도 다양하게 들어올 수 있다
