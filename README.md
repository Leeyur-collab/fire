# fire


yolov8 학습
-->가상화로 돌릴 것
```bash
# 가상환경 생성
python -m venv yolov8_env

# 가상환경 활성화
yolov8_env\Scripts\activate 

# 주피터 설치
pip install jupyter

#주피터 노트북 오픈
jupyter notebook
```
이후 yolov8_fire.ipynb 실행

--> 이 경우 가상환경이 GPU를 못 잡을 수도 있음

만약 못잡으면 다시 cmd 환경에서
```bash 
yolov8_env\Scripts\activate
pip uninstall torch torchvision torchaudio
pip install torch torchvision torchaudio --index-url https://download.pytorch.org/whl/cu118
jupyter notebook
```
파이썬에서 테스트
```python3
import torch
print(torch.cuda.is_available())
print(torch.cuda.current_device())
print(torch.cuda.get_device_name(torch.cuda.current_device()))
```
True
0
NVIDIA GeForce RTX 3090 < 이런 식으로 나오면 할당 잘 된것
