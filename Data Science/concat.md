데이터프레임을 위-아래 또는 왼쪽-오른쪽으로 단순히 연결할 때는 concat을 활용
appetizer = pd.DataFrame({
    'Menu': ['Salad', 'Soup', 'Bread'],
    'Price': [5000, 3000, 2000]
})

main = pd.DataFrame({
    'Menu': ['Steak', 'Pasta', 'Chicken'],
    'Price': [15000, 12000, 10000]
})
full_menu = pd.concat([appetizer, main], ignore_index=True)
![[Pasted image 20260826101917.png]]
기본은 위-아래로 합치는 것이다
full_menu = pd.concat([appetizer, main], axis=1)
![[Pasted image 20260826101949.png]]
왼쪽-오른쪽으로 합치고 싶다면 axis=1을 활용하면 된다.
