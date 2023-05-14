# 토마토 잎 병 분석 분류 모델 제작


   ## 1. 데이터 셋 설명

토마토 잎 병에 대한 데이터셋으로
- https://www.kaggle.com/datasets/kaustubhb999/tomatoleaf

10개의 카테고리로 10000개의 train, 각 카테고리 당 1000장
1000개의 test , 각 카테고리 당 100장으로 구성되어 있습니다. 

![fb73cd43-aa32-4aba-978f-034c9c809c25___RS_HL 9749](https://github.com/yoon0309/Development_of_a_classification_model_for_analyzing_tomato_leaf_diseases/assets/102473586/8d55aa5a-3801-42d7-8aff-b36600834f50) ![ebf036fa-436b-42aa-8a34-0b0f188bc54a___PSU_CG 2134](https://github.com/yoon0309/Development_of_a_classification_model_for_analyzing_tomato_leaf_diseases/assets/102473586/93d30742-0937-4d22-86cd-9b899025084e)![feb8257c-4450-4a09-906d-b1aafd46c301___UF GRC_YLCV_Lab 02953](https://github.com/yoon0309/Development_of_a_classification_model_for_analyzing_tomato_leaf_diseases/assets/102473586/6b5e4248-6bc1-4fe8-adda-b4a63d3e4055)![f9bf89e2-3e30-4b63-832b-ad6247a3ab06___Com G_TgS_FL 0869](https://github.com/yoon0309/Development_of_a_classification_model_for_analyzing_tomato_leaf_diseases/assets/102473586/5b9db9bb-9b9f-46e7-89cc-10f81033269e)![fd2cc1ea-22d9-4c3f-80c6-0c9dc40bdcaa___Com G_SpM_FL 9006](https://github.com/yoon0309/Development_of_a_classification_model_for_analyzing_tomato_leaf_diseases/assets/102473586/c6403340-ebd7-4a73-9148-b9d22aff30c3)![fc963fa5-7179-402b-95e7-018c2837d2c1___JR_Sept L S 2706](https://github.com/yoon0309/Development_of_a_classification_model_for_analyzing_tomato_leaf_diseases/assets/102473586/2705b630-4729-4a45-b302-586f3a0b798e)![fa0cb20b-cafb-494d-85f5-0af1a5785671___Crnl_L Mold 6743](https://github.com/yoon0309/Development_of_a_classification_model_for_analyzing_tomato_leaf_diseases/assets/102473586/4df16635-5e4b-4104-93ed-a713e89907f5)![fc4eb42f-062f-4840-80f5-3244866a1e3a___GHLB2 Leaf 125 2](https://github.com/yoon0309/Development_of_a_classification_model_for_analyzing_tomato_leaf_diseases/assets/102473586/cf44b64a-d09b-4e1f-bc9f-27d2d277b4d1)![f9f35406-f925-4c34-a1f5-0f73563033a0___RS_Erly B 7570](https://github.com/yoon0309/Development_of_a_classification_model_for_analyzing_tomato_leaf_diseases/assets/102473586/a504f555-cf60-42c3-8948-1c08f8814226)![fcff6ccd-294d-481f-affb-815097ed74dc___GCREC_Bact Sp 3115](https://github.com/yoon0309/Development_of_a_classification_model_for_analyzing_tomato_leaf_diseases/assets/102473586/75e82156-bc5d-42e8-903e-14c533c790bb)


카테고리는 Tomato___healthy (건강한 토마토),  Tomatomosaicvirus(토마토 모자이크 바이러스),   TomatoYellowLeafCurlVirus(토마토황화잎말림바이러스), Target_Spot(표적 반점),  Spidermites Two-spottedspider_mite(점박이진드기),  Septorialeafspot - Septorial(잎 반점),   Leaf_Mold(잎 곰팡이),  Late_blight(역병),  Early_blight(토마토 초기 역병),   Bacterial_spot(세균 반점)구성되어 있습니다. 




   ## 2. 프로젝트에서 풀고자 하는 문제 (문제인식, 문제 정의, 가설)

한약재를 감정하는 방법에는 다양한 방법이 존재합니다.  

한약재를 감정하기에 앞서, 중요한 것은 좋은 한약재를 재배하는 것입니다. 

토마토 잎을 보고 토마토의 상태를 알려주는 모델을 통하여 문제 상황에 따른 빠른 확인, 품질과 수량을 높일 수 있습니다. 






   ## 3. 프로젝트 진행과정 


<img width="500" src="https://user-images.githubusercontent.com/102473586/236621189-b0aa897d-8123-4512-b554-eaf06e738ad4.jpg"> 

imagedatagenator로 이미지를 학습 시킬 때 양이 적은 경우 학습 데이터를 조금씩 변형시켜서 학습 데이터의 양을 늘리는 방식을 사용하였으며, Rescale 1./225을 통하여 값을 1과 0 사이의 값으로 변경하였습니다.  





   ## 4. 문제상황 해결과정(분석기법, 모델 등)

<img width="500" src="https://user-images.githubusercontent.com/102473586/236621234-a6f84602-85c8-4826-82f5-e94366f54fd3.png"> 

vgg19모델은 사진을 여러개의 작은 부분으로 나누고 각 부분에서 물체의 특징을 찾아내고 이러한 특징들을 조합하여 사물을 인식하고 물체가 무엇인지 예측하는 모델을 말합니다.  





   ## 5. 결과정리 


![화면 캡처 2023-05-06 202551](https://user-images.githubusercontent.com/102473586/236621299-edb81880-df2b-4303-9b33-2b7abc365409.jpg)

![화면 캡처 2023-05-06 202615](https://user-images.githubusercontent.com/102473586/236621301-58d4b19b-7e81-49c2-b2fd-f7b2edfe3d61.jpg)


학습이 진행될수록 시각화에 나온 것과 같이 **train loss** 는 1.5597에서 **0.4785**로, **val loss**는 1.2061에서 **0.6592**로 감소하였습니다.

**train accuracy**는 0.5534에서 **0.8557**로, **val accuracy**는 0.6380에서 **0.7720**으로 증가하였음을 확인할 수 있습니다.   

<img width="500" src="https://user-images.githubusercontent.com/102473586/236621203-c252d99c-659c-432e-b28c-5f0e45fe33f1.jpg">![236621311-5f40482e-157d-4ae2-8153-1243f2174b1b](https://github.com/yoon0309/Development_of_a_classification_model_for_analyzing_tomato_leaf_diseases/assets/102473586/ff33c944-3def-4482-8770-20738999c3a0)


또한,  각 데이터 카테고리별 0~9까지 라벨링을 통해 어떤 잎을 잘 맞추었는지 확인하였을 때, Leaf_mold - 잎 곰팡이, Target_Spot - 표적 반점, Late_blight 역병 순으로 잘 맞추지 못함을 알 수 있었습니다.





   ## 6. 한계점 및 해결방안 

데이터셋이 작은 문제로 분석에서 더 높은 성능을 내지 못한 것이 아쉽습니다.

또한 분석 시 Epoch가 10임에도, 분석 시간이 너무 오래 걸렸습니다.

이 모델을 기반으로 다른 작물 데이터를 이용하여 잎분석 딥러닝 모델을 확장하여 웹 페이지로 만들어 사진을 입력하면 잎을 통해 어떤 조치를 취해야 할지 알려주는 식으로 모델 발전을 할 수 있을 것입니다.
