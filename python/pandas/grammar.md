

```
fs_df.index = fs_df.index.set_names('종목명')

```


인덱스의 '이름' 바꾸기

---

```
backtest_df = pd.DataFrame({'사과 개수':[apple_pf]},index=[date])
```

데이터프레임을 만들 때는 데이터가 단 하나라도 시리즈형태를 유지해야하므로 무조건 리스트 []로 구성되어야한다. ( 컬럼명 제외 )
