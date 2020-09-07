# Kaggle Global Wheat Detection

## Overview
<p align="center"><img src="https://storage.googleapis.com/kaggle-media/competitions/UofS-Wheat/descriptionimage.png" height="300px"></img></p>

- kaggle [Global Wheat Detection](https://www.kaggle.com/c/global-wheat-detection/overview) competition 참가
- 밀이 촬영된 이미지에서 "밀알(wheat heads)"를 찾아내는 object detection을 수행
- [Global Wheat Head Dataset](http://www.global-wheat.com/2020-challenge/)을 데이터셋으로 사용
- mAP(mean Average Precision)을 통해 최종 평가
- submission 파일의 형식은 이미지 id, confidence score, bounding box의 x좌표, y좌표, width, height을 csv 파일로 제출
- GPU 사용량 6시간 미만, 인터넷 접속 불가, 제출 파일명은 submission.csv


## Project Details
<p align="center"><img src="https://ifh.cc/g/tOvV6W.jpg"></p>

- timm 패키지를 통해 `efficientdet_d5` 모델 사용
- TTA(Test Time Augmentation) 사용(Horizontal Flip, Vertical Flip, Rotation)
- [WBF(Weighted Box Fusion)](https://github.com/ZFTurbo/Weighted-Boxes-Fusion)을 적용함
- Public 453등, Private 503등 달성
