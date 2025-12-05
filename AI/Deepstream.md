# Deepstream
NVIDIA에서 개발한 AI 기반 비디오 분석 SDK(Software Development Kit)  
SDK는 특정 플랫폼, 시스템, 또는 하드웨어에서 애플리케이션을 개발할 때 필요한 라이브러리, API, 문서, 코드 샘플, 디버깅 도구 등을 포함

## 주요특징
1. 고성능 비디오 분석:  
초당 수십 개의 비디오 스트림을 실시간으로 처리할 수 있습니다.  
NVIDIA GPU의 병렬 처리 능력을 활용해 높은 처리량을 제공합니다.  
  
2. AI 및 딥러닝 통합:  
TensorRT를 사용해 딥러닝 모델을 최적화하고 가속화합니다.  
사전 학습된 모델(예: YOLO, SSD, Faster R-CNN)을 쉽게 통합할 수 있습니다.  
  
3. 다양한 입력 소스 지원:  
IP 카메라(RTSP), 파일, USB 카메라 등 다양한 소스에서 비디오를 입력받을 수 있습니다.  
  
4. 모듈식 아키텍처:  
GStreamer 기반의 파이프라인을 사용해 유연하게 비디오 처리 흐름을 구성할 수 있습니다.  
  
5. 크로스 플랫폼 지원:  
Linux 기반 시스템에서 동작하며, NVIDIA Jetson(임베디드) 및 DGX 시리즈(고성능 서버)를 지원합니다.  
  
6. 실시간 객체 탐지 및 추적:  
비디오 스트림에서 객체를 탐지하고 추적하는 기능을 제공합니다.  
  
## DeepStream의 주요 구성 요소
- GStreamer 플러그인  
DeepStream은 GStreamer 프레임워크를 기반으로 구축되었으며, 비디오 처리 파이프라인을 구성합니다.  
  
- DeepStream SDK  
비디오 분석을 위한 API, 라이브러리, 도구를 제공합니다.  
  
- TensorRT
딥러닝 모델을 최적화하고 GPU에서 고속으로 실행합니다.  
  
- NVIDIA Triton Inference Server  
분산 환경에서 딥러닝 모델을 서빙하는 데 사용됩니다.  
  
- NVIDIA DALI  
데이터 전처리를 가속화하는 라이브러리입니다.  