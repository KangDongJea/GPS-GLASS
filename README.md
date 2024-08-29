# QUANTIZATION-FRIENDLY SUPER RESOLUTION: UNVEILING THE BENEFITS OF ACTIVATION NORMALIZATION

## Environments
사용된 환경은 environments.txt 를 확인하시면 됩니다.

## Datasets
DIV2K, Urban100, B100, Set5, Set14 데이터셋이 사용되었으며 폴더 구성 Tree는 다음과 같습니다.

dataset

├── benchmark

│   ├── B100

│   ├── Set14

│   ├── Set5

│   └── Urban100

├── DIV2K

│   ├── bin

│   ├── DIV2K_test_LR_bicubic

│   ├── DIV2K_test_LR_unknown

│   ├── DIV2K_train_HR

│   ├── DIV2K_train_LR_bicubic

│   ├── DIV2K_train_LR_unknown

│   ├── test2k

│   └── test4k


batchnorm

├── DDTB

├── environments.txt

├── experiment

│   ├── EDSR_dBN_x4

│   ├── EDSR_x4

│   └── output

└── PAMS

## Training & Testing
PAMS 및 DDTB 폴더 내부의 train.sh 또는 test.sh를 실행하면 학습 및 테스트를 할 수 있습니다.

## 참고
- experiment 폴더 내부의 EDSR_dBN_x4 및 EDSR_x4 는 각각 BN 포함 유무에 따른 Full-Precision pretrain 파일입니다.
- train.sh를 통해 새로 학습시키는 모델은 experiment/output 폴더 내부에 생성됩니다.
- RDN 등의 모델을 추가적으로 학습시키기 위해서 DDTB 내부의 main_ori.py를 사용하면 됩니다.
- PAMS 및 DDTB의 model 폴더 내부에 각 모델 구조가 구현되어 있습니다. BN이 추가된 모델은 기존 Fake quantization method인 PAMS 및 DDTB에 기반하여 구현되어 있으며, 하드웨어에 따른 실제 양자화 구현을 위해 추가 변형이 요구될 수 있습니다. 
