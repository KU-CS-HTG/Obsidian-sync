[[plot]]의 seaborn 버전으로, 선형 그래프를 그리는데 x, y에 구체적인 거를 넣고 싶으면 lineplot을 활용하는 듯
import seaborn as sns
f, ax = plt.subplots(nrows=2, ncols=1, figsize=(15, 15))
sns.lineplot(x=df.Date, y=old.fillna(np.inf), ax=ax[0], color='darkorange', label = 'original')
sns.lineplot(x=df.Date, y=df.River_Hydrometry.fillna(np.inf), ax=ax[0], color='dodgerblue', label = 'modified')
