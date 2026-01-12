---
citekey: krajewskiHighDDatasetDrone2018
aliases: ["Krajewski et al.å (2018) The highD Dataset"]
title: "The highD Dataset: A Drone Dataset of Naturalistic Vehicle Trajectories on German Highways for Validation of Highly Automated Driving Systems"
authors: Robert Krajewski, Julian Bock, Laurent Kloeker, Lutz Eckstein
tags: [literature-note, ]
year: 2018
publisher: ""
doi: 10.1109/ITSC.2018.8569552
---

# [The highD Dataset: A Drone Dataset of Naturalistic Vehicle Trajectories on German Highways for Validation of Highly Automated Driving Systems](zotero://select/library/items/AU3QG4ZS)

%% begin notes %%

## Key takeaways
- 

## Processing

- **Status**:: 
- **Priority**:: 
- **Connections**:: 
%% end notes %%

> [!info]- Info - [**Zotero**](zotero://select/library/items/AU3QG4ZS) | [**DOI**](https://doi.org/10.1109/ITSC.2018.8569552) | [**PDF**](file:////Users/sanghyun/Library/Mobile%20Documents/com~apple~CloudDocs/Zotero_file/Krajewski%20등%20-%202018%20-%20The%20highD%20Dataset%20A%20Drone%20Dataset%20of%20Naturalistic%20Vehicle%20Trajectories%20on%20German%20Highways%20for%20Valid.pdf)
>
> **Bibliography**: Krajewski, Robert, Julian Bock, Laurent Kloeker와/과Lutz Eckstein. “The highD Dataset: A Drone Dataset of Naturalistic Vehicle Trajectories on German Highways for Validation of Highly Automated Driving Systems”. _2018 21st International Conference on Intelligent Transportation Systems (ITSC)_, IEEE, 2018년 11월, 2118–25. [https://doi.org/10.1109/ITSC.2018.8569552](https://doi.org/10.1109/ITSC.2018.8569552).
> 
> **Authors**::  [[Robert Krajewski]],  [[Julian Bock]],  [[Laurent Kloeker]],  [[Lutz Eckstein]]
> 
> 
> 
> **Collections**:: [[etc]]
> 
> **First-page**: 1

> [!abstract]-
> 

> [!quote]- Citations
> 
> ```query
> content: "@krajewskiHighDDatasetDrone2018" -file:@krajewskiHighDDatasetDrone2018
> ```
 
---
## Reading notes
%% begin annotations %%

*Imported on 2025-11-03 09:56*

### ⭐ Important %% fold %%

- & This approach heavily relies on data from real-world scenarios [(p. 1)](zotero://open-pdf/library/items/L9NHWYLI?page=1&annotation=UDIZNUBS) 
- & However, the current measurement methods fail to meet at least one of the requirements. [(p. 1)](zotero://open-pdf/library/items/L9NHWYLI?page=1&annotation=6GVKWHLJ) 
- & an analysis of extracted lane change maneuvers was performed. [(p. 7)](zotero://open-pdf/library/items/L9NHWYLI?page=7&annotation=SQS5YQHW) 
- **아니 그래서 이 자율주행 안정성 검증을 위한 Dataset은 어디에 쓸 수 있는데??
-> 차선변경 시나리오**:
	- & The frequency distribution of the parameters and parameter combinations can be used as an indication of what kind of lane changes occur under what circumstances. [(p. 7)](zotero://open-pdf/library/items/L9NHWYLI?page=7&annotation=UB77V5XN) 
- & For simplicity, we use a symmetrical model using two separate polynomials for the longitudinal and lateral movement. [(p. 7)](zotero://open-pdf/library/items/L9NHWYLI?page=7&annotation=NHFHQH6B) 
- & quadratic polynomial for the longitudinal movements [(p. 7)](zotero://open-pdf/library/items/L9NHWYLI?page=7&annotation=5EWFMRDH) 
- & polynomial of degree five is used for the lateral movement, [(p. 7)](zotero://open-pdf/library/items/L9NHWYLI?page=7&annotation=83VN6PYS) 
- & The extracted parameters include the minimal DHW, THW, TTC and the gap size [(p. 7)](zotero://open-pdf/library/items/L9NHWYLI?page=7&annotation=RYYN8Z9K) 
- & From the 5600 parameterized lane changes in highD we extracted 850 cut-in scenarios from the right-hand side. [(p. 7)](zotero://open-pdf/library/items/L9NHWYLI?page=7&annotation=L5N7J2VU) 

> [!cite]+ Image [(p. 7)](zotero://open-pdf/library/items/L9NHWYLI?page=7&annotation=6T8T4EFA)
> ![[Zotero/images/image-7-x312-y52.png]]
> **a) 상단 그래프: Cut-in THW Distribution (끼어들기 THW 분포) <b>의미:</b> 다른 차량이 내 앞으로 끼어들 때, 그 순간의 차두시간(THW) 분포 <b>

주요 발견:</b> <b>가장 많은 경우: 0.8~1.0초</b> (최빈값)대부분 <b>0.5~2.5초</b> 사이에 분포0.5초 미만의 매우 위험한 끼어들기도 약 4% 존재4초 이상의 여유 있는 끼어들기는 드뭄 <b>

해석:</b> 실제 고속도로에서 운전자들은 약 1초 정도의 간격만 있어도 끼어든다이는 자율주행 시스템이 대비해야 할 현실적인 상황

b) 하단 그래프: Cut-in THW Dependency on Ego Speed (자차 속도에 따른 THW 의존성)
<b>
X축:</b> 자차(뒤에 있던 차량)의 속도 (km/h) <b>Y축:</b> 끼어들기 시 THW (초) <b>
검은 점선:</b> 중앙값(median) <b>색 음영:</b> 십분위수(deciles) - 데이터의 분포 범위 <b>
주요 발견:</b> 속도가 빠를수록 THW가 약간 증가하는 경향90km/h: 중앙값 약 1.2초160km/h: 중앙값 약 2.2초하지만 속도에 관계없이 <b>매우 넓은 분포</b> (0.5초~5초)
<b>
해석:</b> 속도가 빠를수록 운전자들이 조금 더 여유 있게 끼어들지만여전히 위험한 끼어들기(1초 미만)는 모든 속도에서 발생자율주행 차량은 <b>모든 속도 구간에서 다양한 THW의 끼어들기</b>에 대비해야 함**

### 💡 Main ideas and conclusions %% fold %%

- $ measure data from an aerial perspective [(p. 1)](zotero://open-pdf/library/items/L9NHWYLI?page=1&annotation=CD2W3SBA) 
- $ Thus, we propose to use camera-equipped drones to measure every vehicle’s position and movements from an aerial perspective for scenario-based validation. [(p. 1)](zotero://open-pdf/library/items/L9NHWYLI?page=1&annotation=TU5DSMQT) 

> [!cite]+ Image [(p. 2)](zotero://open-pdf/library/items/L9NHWYLI?page=2&annotation=LULYM9V6)
> ![[Zotero/images/image-2-x32-y528.png]]
> **"자율주행 시나리오"를 체계적으로 설명하기 위한 프레임워크**
- $ the lateral movement is more relevant for lane changes. [(p. 7)](zotero://open-pdf/library/items/L9NHWYLI?page=7&annotation=GHD8HTXV) 
- $ detecting the lane changes by lane crossings [(p. 7)](zotero://open-pdf/library/items/L9NHWYLI?page=7&annotation=PVBQVS5F) 
- **분석 목적: <b>유발 조건 분석</b>: 왜 차선을 변경했는가? 예: 앞차가 느려서, 뒷차가 너무 가까워서 <b>

위험도 평가</b>: 얼마나 위험한 차선 변경인가? 예: TTC가 2초 이하면 위험한 상황 이를 통해

실제 도로에서 일어나는 다양한 차선 변경 상황의 특성과 위험도를 정량적으로 파악할 수 있다.**:
	- $ As shown in [4], these parameters allow an analysis of the inducing conditions and an assessment of the criticality of the performed lane change. [(p. 7)](zotero://open-pdf/library/items/L9NHWYLI?page=7&annotation=UJEQD33X) 

> [!cite]+ Image [(p. 7)](zotero://open-pdf/library/items/L9NHWYLI?page=7&annotation=7NQW7RQB)
> ![[Zotero/images/image-7-x40-y56.png]]
> ****

### ⛔ Weaknesses and caveats %% fold %%

- ! However, existing methods and tools for the safety validation process are not suitable for the complexity of these systems and would be inefficient with regard to costs and time resources [(p. 1)](zotero://open-pdf/library/items/L9NHWYLI?page=1&annotation=S5F6JWHC) 
- ! because of the sensors’ physical limitations and the visibility of the sensors. [(p. 1)](zotero://open-pdf/library/items/L9NHWYLI?page=1&annotation=63ML9VBF) 
- **차량 높이는 포기하지만,
차량 type으로 높이 추정 가능**:
	- ! However, an object’s height has only limited relevance for safety validation and can be estimated from the object type. [(p. 1)](zotero://open-pdf/library/items/L9NHWYLI?page=1&annotation=5IUWWDLS) 


%% end annotations %%

%% Import Date: 2025-11-03T09:57:00.102+09:00 %%
