# 토마토 잎 병 분석 분류 모델 제작

1. 데이터 셋 설명  

토마토 잎 병에 대한 데이터셋으로
- https://www.kaggle.com/datasets/kaustubhb999/tomatoleaf

10개의 카테고리로 10000개의 train, 각 카테고리 당 1000장
1000개의 test , 각 카테고리 당 100장으로 구성되어 있습니다. 

카테고리는 Tomatomosaicvirus(토마토 모자이크 바이러스), Target_Spot(표적 반점),  Bacterial_spot(세균 반점), TomatoYellowLeafCurlVirus(토마토황화잎말림바이러스),
Late_blight(역병), Leaf_Mold(잎 곰팡이), Early_blight(토마토 초기 역병), Spidermites Two-spottedspider_mite(점박이진드기), Septorialeafspot - Septorial(잎 반점), Tomato___healthy (건강한 토마토)로 구성되어 있습니다.

2. 프로젝트에서 풀고자 하는 문제 (문제인식, 문제 정의, 가설)

한약재를 감정하는 방법에는 다양한 방법이 존재하는데 

한약재를 감정하는 것에 1차적으로 중요한 것은 좋은 한약재를 재배하는 것입니다. 

토마토 잎을 보고 토마토의 상태를 알려주는 모델을 통하여 문제 상황에 따른 빠른 확인, 품질과 수량을 높일 수 있습니다. 

3. 프로젝트 진행과정 

 imagedatagenator로 이미지를 학습 시킬 때 양이 적은 경우 학습 데이터를 조금씩 변형시켜서 학습 데이터의 양을 늘리는 방식

Rescale 1./225는 값을 1과 0 사이의 값으로 변경하는 것을 말함 

4. 문제상황 해결과정(분석기법, 모델 등)

vgg19모델은 사진을 여러개의 작은 부분으로 나누고 각 부분에서 물체의 특징을 찾아내고 이러한 특징들을 조합하여 사물을 인식하고 물체가 무엇인지 예측하는 모델 

5. 결과정리 

학습이 진행될 수록 train loss, test loss가 감소하였고 train 정확도, test 정확도가 올라가서 최종적으로 85%의 정확도를 가질 수 있었습니다. 

6. 한계점 및 해결방안 

분석시 Epoch가 10임에도, 분석시간이 너무 오래걸렸으며, 한약재가 위조 한약재인지 1,0으로 나누는 이진분류 모델을 만들고 싶었지만 데이터셋의 구하기 어려움을 느꼈습니다. 

이 모델을 기반으로 다른 작물 데이터를 이용하여 잎 분석 딥러닝 모델을 확장하여 웹 페이지로 만들어 사진을 입력하면 잎을 통해 어떤 조치를 취해야할지 알려주는 식으로 모델 발전을 할 수 있을 것입니다.
