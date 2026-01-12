 

> **Goal**: Image, Video, Tabular 데이터를 아우르는 Anomaly Detection(AD) Master Plan
> **Tags**: #Research #AnomalyDetection #DeepLearning #GraduateSchool

---

## Phase 1: Foundations & Survey (기초 및 흐름 파악)
딥러닝 이전의 통계적 방법론과 최신 딥러닝 기법의 전체적인 숲을 보는 단계입니다.

### 🏛 The Classics (Must Read for Definitions)
- [ ] **Anomaly Detection : A Survey** (Chandola et al., 2009)
	- *Note*: **[필독]** AD 분야의 구약성서. 이상치의 3가지 타입(Point, Contextual, Collective) 정의를 여기서 배울 것. 논문 작성 시 인용 필수.

### 🗺 Modern Deep Learning Surveys
- [ ] **Deep Learning for Anomaly Detection: A Review** (Pang et al., 2021)
	- *Note*: 딥러닝 AD 전반을 아우르는 교과서.
- [ ] **Deep Industrial Image Anomaly Detection: A Survey** (Tao et al., 2023)
	- *Note*: **[강추]** Image/Manufacturing 분야 최신 트렌드 정리. Phase 2 진입 전 필독. PatchCore, PaDiM 등의 계보를 파악하기 좋음.
- [ ] **Deep Learning for Time Series Anomaly Detection: A Survey** (Choi et al., 2021 / Schmidl et al., 2022)
	- *Note*: 시계열 데이터(Tabular/Sensor)에서 Reconstruction 및 Prediction 기반 방법론 비교.

### 🏛 Classical Baselines (Deep Learning 이전)
- [ ] **Isolation Forest** (Liu et al., ICDM 2008) #Tabular
	- *Key*: "이상치는 고립(Isolate)시키기 쉽다". Tree 기반 베이스라인.
- [ ] **SVDD (Support Vector Data Description)** (Tax & Duin, 2004)
	- *Key*: 정상 데이터를 감싸는 가장 작은 구(Hypersphere)를 찾는 One-Class Classification.

---

## Phase 2: Image Anomaly Detection (핵심 연구 분야)
가장 많은 연구가 진행된 분야입니다. Reconstruction에서 Feature Embedding으로 넘어가는 흐름을 파악하세요.

### 🛠 Reconstruction-based (복원 기반)
- [ ] **AnoGAN** (Schlegl et al., IPMI 2017)
	- *Key*: GAN을 AD에 최초 적용. (역사적 의미)
- [ ] **f-AnoGAN** (Schlegl et al., Medical Image Analysis 2019)
	- *Key*: AnoGAN의 느린 추론 속도 개선.
- [ ] **MVTec AD Benchmark Paper** (Bergmann et al., CVPR 2019)
	- *Key*: AE(L2 + SSIM loss) 베이스라인 및 데이터셋 소개.
- [ ] **DRAEM** (Zavrtanik et al., ICCV 2021)
	- *Key*: 인위적인 이상(Anomaly)을 합성하여 Denoising Autoencoder로 복원 학습.

### 🧠 Embedding & Memory-based (임베딩 및 메모리)
- [ ] **Deep SVDD** (Ruff et al., ICML 2018) #MustRead
	- *Key*: 고전 SVDD의 Deep Learning 버전. Center Loss 개념.
- [ ] **SPADE** (Cohen et al., 2020)
	- *Key*: ImageNet Pre-trained Feature를 픽셀 단위로 매칭 (KNN).
- [ ] **PaDiM** (Defard et al., ICPR 2021) #HighlyRecommended
	- *Key*: 각 패치 위치의 다변량 가우시안 분포 모델링.
- [ ] **PatchCore** (Roth et al., CVPR 2022) #SOTA #MustImplement
	- *Key*: Memory Bank + Coreset Sampling. 현업 최강 성능 및 속도 균형.
- [ ] **CFA** (Lee et al., 2022)
	- *Key*: PatchCore의 메모리 뱅크를 압축하여 속도 개선.

### 🌊 Normalizing Flow & Distillation
- [ ] **FastFlow** (Yu et al., 2021)
	- *Key*: 2D Normalizing Flow를 사용하여 복잡한 분포 추정.
- [ ] **CS-Flow** (Rudolph et al., WACV 2022)
	- *Key*: Multi-scale feature를 활용한 Flow 모델.
- [ ] **SimpleNet** (Liu et al., CVPR 2023)
	- *Key*: 간단한 구조의 Feature Adapter와 인공 노이즈를 활용해 SOTA 달성.

---

## Phase 3: Video Anomaly Detection (심화 연구)
이미지 + 시간(Temporal) 정보를 다룹니다. CCTV 서베일런스 연구의 핵심입니다.

### 📹 Weakly Supervised (MIL 기반)
- [ ] **Real-world Anomaly Detection in Surveillance Videos** (Sultani et al., CVPR 2018) #MustRead
	- *Key*: Video-level Label만으로 이상 구간을 탐지(MIL). UCF-Crime 데이터셋 공개.
- [ ] **RTFM** (Tian et al., ICCV 2021)
	- *Key*: 이상(Top-k scores)과 정상의 Feature Magnitude 차이를 최대화.

### 📼 Reconstruction & Prediction
- [ ] **Future Frame Prediction for AD** (Liu et al., CVPR 2018)
	- *Key*: 다음 프레임 예측 오차를 이용한 탐지.
- [ ] **MemAE (Memory-augmented Autoencoder)** (Gong et al., ICCV 2019) #MustRead
	- *Key*: AE가 이상치도 복원하는 문제 해결 -> '정상 패턴 메모리' 도입.
- [ ] **MNAD** (Park et al., CVPR 2020)
	- *Key*: Memory module을 고도화하여 Prediction/Reconstruction에 모두 적용.

### 🚀 Spatiotemporal Transformer (SOTA)
- [ ] **VideoMAE V2** (Wang et al., CVPR 2023)
	- *Key*: Masked Autoencoder의 비디오 버전. 대규모 데이터 학습.
- [ ] **UBnormal** (Acsintoae et al., CVPR 2022)
	- *Key*: 가상의 이상 데이터를 생성(Simulation)하여 Supervised처럼 학습.

---

## Phase 4: Time-Series & Tabular (특수 도메인)
정형 데이터와 시계열 로그 분석을 위한 연구입니다.

### 📈 Time-Series
- [ ] **OmniAnomaly** (Su et al., KDD 2019)
	- *Key*: Stochastic RNN 기반의 다변량 시계열 AD.
- [ ] **USAD** (Audibert et al., KDD 2020)
	- *Key*: AE + GAN 구조를 결합하여 빠르고 안정적.
- [ ] **Anomaly Transformer** (Xu et al., ICLR 2022) #MustRead
	- *Key*: Association Discrepancy(전체 흐름 vs 인접 흐름) 차이 이용.
- [ ] **TimesNet** (Wu et al., ICLR 2023)
	- *Key*: 1D 시계열을 2D 텐서로 변환하여 Inception Block 적용.

### 📋 Tabular (Deep Learning)
- [ ] **DAGMM** (Zong et al., ICLR 2018)
	- *Key*: Autoencoder + GMM의 End-to-End 학습.
- [ ] **GOAD** (Bergman et al., ICLR 2020)
	- *Key*: 데이터 변환(Transformation) 분류 문제를 통한 이상치 탐지.
- [ ] **NeuTraL AD** (Qiu et al., ICML 2021)
	- *Key*: Learnable Transformation을 이용한 Contrastive Learning.

---

## Phase 5: Advanced Topics (최신 트렌드)
남들이 안 한 연구 주제를 찾고 싶다면 이쪽을 파야 합니다.

### 🤖 Zero-shot / Few-shot & VLM
- [ ] **WinCLIP** (Jeong et al., CVPR 2023)
	- *Key*: CLIP(Language-Image)을 활용한 Zero-shot AD. Text Prompt 활용.
- [ ] **Segment Any Anomaly** (Cao et al., 2023)
	- *Key*: Segment Anything Model (SAM)과 GroundingDINO 결합.

### 🧩 Logical Anomaly Detection
- [ ] **MVTec LOCO AD** (Bergmann et al., IJCV 2022)
	- *Key*: 구조적/논리적 이상(Logical Anomaly) 데이터셋 및 베이스라인.

---

## 💾 Essential Resources

### Datasets
- [ ] **MVTec AD**: 이미지 AD 표준 (제조).
- [ ] **VisA**: 복잡한 구조의 이미지 데이터.
- [ ] **UCF-Crime**: 비디오 AD 표준 (CCTV).
- [ ] **ShanghaiTech**: 캠퍼스 내 이상 행동 비디오.
- [ ] **SWaT / WADI**: 수처리 시설 센서 데이터 (Time-series).

### Code Libraries
- [ ] **Anomalib (Intel)**: [Github Link](https://github.com/openvinotoolkit/anomalib) - Image AD 모델 집합소.
- [ ] **PyOD**: [Github Link](https://github.com/yzhao062/pyod) - Tabular/Multivariate AD 라이브러리.
- [ ] **DeepOD**: [Github Link](https://github.com/xuhongzuo/DeepOD) - Deep Learning Tabular AD.