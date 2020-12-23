# Korea-univ-2020
자연어처리 한국어(nsmc) / 영어(emotionlines) 감정 분류 모델링

한국어 감성 분류 모델은 KoBERT를 사용하였습니다. 
영어 감정 분류 모델은 electra를 활용하였습니다. 

Requirements
- transformers == 2.10.0 
- PyTorch == 1.0.1
- TensorFlow == 2.0.0

학습환경 : AWS p3.16xlarge(GPU:8, CPU:64, MEMORY:488G - Tesla V100)

1. 한국어 모델 실행 방법
 
 (1) 모델 학습

python3 main.py --model_type kobert --do_train --do_eval --num_train_epochs 24
 
 (2) 답안 구현
 
 python3 predict.py --input_file ko_data1.txt --output_file pred_1217_kobert_epo24.txt --model_dir model/
 
 2. 영어 모델 실행 방법
 ipynb 소스 파일 실행
