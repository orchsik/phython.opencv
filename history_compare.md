## 히스토그램 비교를 통한 이미지 유사도 

- 히스토그램은 이미지의 픽셀 값의 분포를 나타낸다.  
- 픽셀 값의 분포가 서로 비슷하면 유사한 이미지일 확률이 높고, 분포가 서로 다르면 서로 다른 이미지일 확률이 높습니다.  
- 이러한 사실을 이용하여 이미지의 유사도를 측정할 수 있다.  

```python
cv2.compareHist(hist1, hist2, method)
```
- hist1, hist2: 비교할 두 개의 히스토그램, 크기와 차원이 같아야 함  
- method: 비교 알고리즘  
  - cv2.HISTCMP_CORREL: 상관관계 (1: 완전 일치, -1: 완전 불일치, 0: 무관계)  
  - cv2.HISTCMP_CHISQR: 카이제곱 (0: 완전 일치, 무한대: 완전 불일치)  
  - cv2.HISTCMP_INTERSECT: 교차 (1: 완전 일치, 0: 완전 불일치 - 1로 정규화한 경우)

 