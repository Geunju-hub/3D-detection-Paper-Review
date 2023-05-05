# MMdetection3D를 이용한 실습
-----------------------------------------
## week. 7
환경설정 구축
1. 4명(백근주, 김대식, 박민배, 박준서) 는 Colab pro 환경에서, 1명(김동영) 은 Desktop 환경에서 진행하기로 결정함
2. 라이브러리는 MMdetection3d를 사용하기로 결정함
3. 기본적인 Config 파일 구성 및 실제 내부 인자에 대해 공부함.
------------------------------------------------
## week. 8
1. Baseline은 MMdetection3d의 pointpillars_hv_secfpn_8xb6-160e_kitti-3d-3class.py를 Baseline으로 정함
2. 해당 github에 저장되어있는 pre-train model이 아닌 Colab pro를 이용하여 직접 학습시킨 모델을 baseline으로 설정함

------------------------------------------------
## week. 9
1. 각자 Baseline이 잘 동작했는지 여부 확인
2. 각자 Baseline보다 성능을 어떻게 더 높일지 근거(논문, 실험표)를 토대로 계획 세움
------------------------------------------------
## 모델 개선 방법

| 이름 | 주차 | 개선 방법 | 관련 자료 링크 |
| :--: | :--: | :------: | :------------: |
| 백근주 | 9 | PillarNet 논문, CenterPoint 논문 → CenterPoint KITTI로 확인 | [Paper](https://arxiv.org/pdf/2205.07403.pdf) |
| 김대식 | 9 | PointPillar의 backbone에 따른 성능 및 속도 차이 관련 논문 → CSPdarknet으로 성능 향상 확인 | [Paper](https://arxiv.org/pdf/2209.15252.pdf) |
| 김동영 | 9 | PointPillar의 backbone에 따른 성능 및 속도 차이 관련 논문 → CSPdarknet으로 성능 향상 확인 | [Paper](https://arxiv.org/pdf/2209.15252.pdf) |
| 박준서 | 9 | Point cloud 에서 MixUp이 가능함 → Xception 관련해서 구현 및 성능 변화 확인 | [Paper](https://arxiv.org/pdf/2008.06374.pdf) |
| 박민배 | 9 | BatchNorm 적용 위해서 Batch size, Optimizer, 등 기본적인 하이퍼파라미터 튜닝 | [Paper](https://arxiv.org/pdf/1502.03167.pdf) |


----------------------------------------------------------------
# 성능표
| Name | Week | Model | Optimizer | Batch size | Learning rate | Scheduler | Epochs | Overall 3D AP@40 | Easy | Moderate | Hard | Model | 
|:---: | :---: | :---: | :--------:| :---------:| :-----------: | :-------: | :----: | :--------------: | :--: | :------: | :--: | :--: |
| X | 8 | Baseline(w/o plane information) | AdamW | 6 | 0.001 | CosineAnnealingLR | 160 | | 65.5701 | 54.9237 | 51.5132 | [Model](https://drive.google.com/file/d/1TnQbvm3nCYMMiUrO_cu2UBM86FeF9itQ/view?usp=sharing)
