# 혼동 행렬의 4가지 주요 지표

## 혼동 행렬 (Confusion Matrix)
모델의 성능을 평가할 때 사용되는 지표로, 예측 값이 실제 관측 값을 얼마나 정확히 맞췄는지를 행렬 형태로 나타낸 것이다.

|               | 예측: 예 (Positive) | 예측: 아니오 (Negative) |
|---------------|---------------------|--------------------------|
| 실제: 예      | TP (True Positive)  | FN (False Negative)      |
| 실제: 아니오  | FP (False Positive) | TN (True Negative)       |

- **TP** : 실제도 예 예측도 예 – 모델이 정답을 맞춘 경우  
- **TN** : 실제도 아니오 예측도 아니오 – 모델이 정답을 맞춘 경우  
- **FP** : 실제는 아니오인데 모델이 예라고 잘못 예측한 경우 (**거짓 양성**)  
- **FN** : 실제는 예인데 모델이 아니라고 잘못 예측한 경우 (**거짓 음성**)  
## 정확도 (Accuracy)
모델이 전체 데이터 중에서 얼마나 정확히 예측했는지를 나타내는 지표  
```text
Accuracy = (TP + TN) / (TP + TN + FP + FN)
```
## 정밀도 (Precision)
모델이 양성이라고 예측한 것들 중 실제로 양성인 비율<br>
즉 예측이 얼마나 신뢰할 수 있는지를 나타냄
```text
Precision = TP / (TP + FP)
```
## 재현율 (Recall, Sensitivity)
실제 양성 중에서 모델이 정확히 양성이라고 예측한 비율
```text
Recall = TP / (TP + FN)
```

## F1 점수 (F1 Score)
정밀도와 재현율의 평균 <br>
두 지표가 모두 중요할 때 사용
```text
F1 Score = 2 * (Precision * Recall) / (Precision + Recall)
```