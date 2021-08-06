


# 다중 컬럼의 구조

<img width="477" alt="스크린샷 2021-08-06 오후 12 44 42" src="https://user-images.githubusercontent.com/88417854/128452937-0c948b9c-3b1b-470e-b6f4-34d7f383d9a6.png">

<br>

```

price_df.columns

```
<br>
                
<img width="516" alt="스크린샷 2021-08-06 오후 12 43 27" src="https://user-images.githubusercontent.com/88417854/128452837-640bc5e1-2712-425c-9340-608a1bdb50ea.png">

<br>

다중 컬럼은 이런식으로 튜플로 저장되어 있다.

이중에서 위에 큰 컬럼 말고 밑에 작은 컬럼 중 하나만을 뽑아서 보기위해선

<br>

```python

for col in price_df.columns:
        if '종가' in col:
         new_col.append(col)
                
price_df[new_col]

```

<br>

즉 컬럼에 있는 값들인 ('A098120 마이크로', '시가'), ('A098120 마이크로', '거래량'), ('A098120 마이크로', '종가') 이것 들 중

price_df[ (('A098120 마이크로', '종가') ] 튜플값인 컬럼을 넣어서 그것만 가져오면 된다.


다중컬럼이 아닐때 price_df['컬럼명']이나 price_df[컬럼리스트] 를 통해 불러오는 것과 똑같다. 튜플값으로 정확히 입력만 하면 된다.






