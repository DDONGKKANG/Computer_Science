# 데이터시각화
**어떤 것들을 그릴 수 있냐** 가 중점!

## treemap
```
treemap(원본, index=c(“배치 기준”), vSize=”타일 크기”   # 원본은 맨 앞에!

```

## 버블차트(bubble chart)
- 산점도(점 대신 텍스트) + 추가 정보 1개 더

## 모자이크 플롯	
```
mosaicplot(~x축+y축, data=원본)
```

## ggplot
```
ggplot(원본, aes(x=x축, y=y축) + geom_bar() )
```
- geom_bar() : 바그래프
- geom_histogram() : 히스토그램
- geom_porint() : 산점도
- geom_boxplot() : 박스그래프
- geom_line() : 선 그래프


