복잡한 데이터를 간단한 표로 요약하여, 중요한 통계치를 한눈에 볼 수 있도록 하는 것
![[Pasted image 20260826103054.png]]
pt = df.pivot_table(index='부서', values='급여', aggfunc='mean')
![[Pasted image 20260826103122.png]]
피벗 테이블을 만들면 이렇게 간단하게 요약할 수 있다
위처럼 단순한 pivot table에 접근할 때는 pt['개발'] 입력하면 옆에 있는 급여가 출력됨 

**피벗 테이블 구성 요소**
index: 데이터의 그룹 기준이 되는 열
columns: 추가적으로 데이터의 세부 항목을 배치하고 싶을 때 사용
ex)부서 안에서 성별, 직급에 따른 데이터를 구분하고 싶다면 부서를 index로 두고, 성별이나 직급을 columns로 두면 된다
values: 집계할 대상
aggfunc: 데이터를 어떻게 요약할지 결정 (mean, sum, min, max 등)

피벗 테이블을 만들다 보면 해당하는 항목이 없어서 NaN으로 나오는 부분이 있는데, 그럴 때는 fill_value=0으로 대체해주는 것이 좋다.
pt = pd.pivot_table(
    df,
    values='수량',
    index=['구분', '유형'],
    columns=['크기'],
    aggfunc="sum",
    fill_value=0
)
![[Pasted image 20260826103619.png]]