🥷 Copy Ninja Bakakashi (카피닌자 바카카시)
"이것이 AI 사륜안의 힘이다." > YOLOv8을 활용한 실시간 나루토 인(Hand Seal) 인식 및 VFX 발동 프로그램
📌 Project Overview
카메라로 인(Hand Seal)을 맺으면 AI가 이를 실시간으로 인식하여 화면에 화려한 인술 이펙트를 띄워주는 프로젝트입니다. 객체 인식 파이프라인을 구축하고, 인터랙티브한 시각 효과를 구현하는 것을 목표로 합니다. 
✨ Key Features
•	Real-time Hand Seal Detection: YOLOv8 기반의 12지신 인 인식
•	Jutsu Sequence Logic: 특정 순서대로 인을 맺을 시 기술 발동 (Queue 자료구조 활용)
•	VFX Overlay: OpenCV를 활용한 실시간 화둔/뇌둔 등의 특수효과 합성
•	Audio Feedback: 기술별 시그니처 사운드 출력
🛠 Tech Stack
•	AI Model: YOLOv8 (Nano/Small)
•	Training: Google Colab (GPU)
•	Dataset: Roboflow
•	Library: OpenCV, PyTorch, MoviePy/Pygame
•	Environment: macOS (Apple Silicon / MPS 가속 활용)
🚀 Getting Started
1. Clone the repository
git clone https://github.com/사용자계정/copy-ninja-bakakashi.git
cd copy-ninja-bakakashi

2. Environment Setup
# 가상환경 생성 및 활성화 권장
python -m venv venv
source venv/bin/activate

# 필요 라이브러리 설치
pip install ultralytics opencv-python torch torchvision

3. Training (Google Colab)
train.ipynb 파일을 사용하여 Google Colab 환경에서 모델을 학습시킨 후, 생성된 best.pt 파일을 weights/ 디렉토리에 저장
4. Run
python main.py

📂 Directory Structure
copy-ninja-bakakashi/
├── data/               # 데이터셋 관련 파일 (YAML 등)
├── weights/            # 학습된 모델 가중치 (.pt)
├── effects/            # VFX 이미지 및 사운드 리소스
├── scripts/            # 유틸리티 스크립트
├── main.py             # 메인 실행 파일
└── train.ipynb         # 학습용 주피터 노트북
