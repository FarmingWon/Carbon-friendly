# learning-passage
The process involves measuring the carbon emissions generated from deep learning training. If a server's training process produces high carbon emissions, we transfer the workload to servers with lower carbon emissions. Ultimately, this method aims to achieve a carbon net-zero state.

# 탄소 친화적 딥러닝 워크로드를 위한 시공간 이동 및 최적화 SW
팀 명 (팀원) : Carbon Watch (박정현, 김대로, 공지환, 이수원, 김채은)

## 1. 프로젝트 소개
본 프로젝트는 딥러닝 모델 학습 시에 비효율적인 GPU 사용을 최소화하기 위하여 전력 소모량과 탄소 배출량을 모니터링하고 전력수요 및 전력 안정성에 최적화된 학습 스케줄을 제공하기 위해 만들어졌습니다.   
 인공지능 컴퓨팅 산업의 급격하게 성장하면서 GPU 사용으로 인한 전력 소모량이 큰 폭으로 증가하였습니다. 대규모 딥러닝 모델의 학습 시 GPU 성능을 우선 시 하기 때문에 성능 대비 전력의 소모량이 크고, 비효율적입니다. 따라서 많은 전력을 필요로 하는 딥러닝 모델 학습의 특성으로 인해 전력 소비를 고려한 DL 학습의 필요성이 부각되고 있습니다.   
 전력 수요가 많아 안정성이 시간대에 GPU 점유율, 프로세스 수를 제한하여 일정 수준으로 낮추는 방법을 제안하고 있습니다. 전력 부하가 많은 시간에는 딥러닝 학습을 줄이고, 전력 부하가 적은 시간대에 집중적으로 학습함으로써, 전력 소비량을 줄일 수 있게 됩니다. 최종적으로 딥러닝 학습의 성능과 전력 소모를 줄일 수 있는 절충점을 찾는 것이 목적입니다.  

## 2. 사용된 기술
다음은 이 프로젝트에서 사용된 주요 기술들입니다:
- [Dash(Plotly)] : Plotly를 기반으로 하는 웹 프레임워크. Dash를 활용하여 Dashboard 제작.
- [firebase] : Google에서 제공하는 모바일 및 웹 애플리케이션 개발 플랫폼. 실시간 데이터베이스와 같은 다양한 서비스를 제공하여 안전하고, 확장 가능한 애플리케이션 구축.
- [FastAPI] : 웹 프레임워크. 강력한 데이터 검증과 자동 문서화 기능을 제공하여 안정성 강화.
- [nvml] : NVIDIA가 제공하는 NVIDIA GPU 드라이버와 상호 작용하는 라이브러리. GPU의 성능 및 상태 정보에 접근하여 시스템에서 GPU 리소스를 효과적으로 관리. GPU 코어 주파수 측정(nvidia-semi)
- [스케줄러] : 작업을 주기적으로 실행하거나 이벤트에 따라 실행하기 위한 도구. 배치 작업을 자동으로 예약 및 실행하는 데 사용. 훈련 과정의 일부를 시·공간적으로 이동.
- [DVFS] : 동적으로 GPU 전압과 주파수를 조절하여, 성능과 전력 소모를 함께 조절하는 기술.
- [L-BFGS] : 주파수를 최적화하기 위한 알고리즘으로 사용.

## 3. 웹 사이트 이미지

![image](https://github.com/jhparkland/learning-passage/assets/86312443/a1afabc7-c56a-4c7e-87b5-deb7c0184556)
