![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54)
![TensorFlow](https://img.shields.io/badge/TensorFlow-%23FF6F00.svg?style=for-the-badge&logo=TensorFlow&logoColor=white)
![PyTorch](https://img.shields.io/badge/PyTorch-%23EE4C2C.svg?style=for-the-badge&logo=PyTorch&logoColor=white)
![NumPy](https://img.shields.io/badge/numpy-%23013243.svg?style=for-the-badge&logo=numpy&logoColor=white)
![Pandas](https://img.shields.io/badge/pandas-%23150458.svg?style=for-the-badge&logo=pandas&logoColor=white)


## Performance & Visual Results

### 1. Qualitative Pose Estimation Outputs
Visual validation across different markerless tracking frameworks:

| MoveNet (17 Body Keypoints) | MediaPipe Holistic (Pose + Hands + 468 Face Mesh) |
| :---: | :---: |
| <img width="438" alt="MoveNet Qualitative" src="https://github.com/user-attachments/assets/701c0023-b4f9-4821-86ad-b23d9096e0bb" /> | <img width="485" height="268" alt="Captura de pantalla 2026-09-23 a las 16 56 10" src="https://github.com/user-attachments/assets/bd30dd36-331c-4301-93ce-33639690618e" /> |
| *Bottom-up single-person pose detection running MobileNetV2 backbone.* | *Multi-stage topology tracking full-body motion, gesture, and facial contours.* |

---

### 2. Apple Silicon ARM CPU Benchmarks (M1 vs M3)
Due to Metal backend library constraints, all pipelines were benchmarked purely on CPU across various video test sequences.

#### MoveNet Lightning Performance (FPS & CPU Usage)
| Architecture Comparison: M1 vs M3 (MoveNet Lightning) |
| :---: |
| <img width="1166" alt="MoveNet Benchmark" src="https://github.com/user-attachments/assets/63e06618-6c0c-47c9-8970-e178e85618ee" /> |
| *M3 achieves slightly higher peak framerates (~25-30 FPS), while complex dynamic sequences throttle both architectures similarly.* |

#### MediaPipe Holistic & Resource Utilization
| MediaPipe Framerate & CPU Scaling | Memory Footprint (RAM) & Model Confidence |
| :---: | :---: |
| <img width="580" alt="MediaPipe CPU & FPS" src="https://github.com/user-attachments/assets/79b5fe90-efab-4ffb-9a4c-772ca905e414" /> | <img width="580" alt="MediaPipe RAM & Confidence" src="https://github.com/user-attachments/assets/a9d005b0-6235-472e-9e88-0c223d98ba3d" /> |
| *MediaPipe peaks at ~20-21 FPS, falling to ~5 FPS under heavy dynamic motion.* | *Identical algorithmic confidence across chips, with M3 exhibiting lower baseline RAM consumption.* |

---

### 3. Pipeline Specifications Summary

| Feature / Metric | MoveNet Lightning | MoveNet Thunder | MediaPipe Holistic | YOLOv8n + MediaPipe |
| :--- | :---: | :---: | :---: | :---: |
| **Input Resolution** | 192 × 192 px | 256 × 256 px | Dynamic | Dynamic (Cropped ROI) |
| **Target Workload** | Ultra-low latency | High precision | Multi-modal full body | Multi-person tracking |
| **Keypoints Tracked** | 17 body joints | 17 body joints | 543 (Pose + Hands + Face) | 33 joints per detected person |
| **Primary Execution** | CPU (Single person) | CPU (Single person) | CPU (Graph pipeline) | Hybrid CPU (YOLO detection + Pose) |

## Authors
- **Rebecca Spiga** - [GitHub Profile](https://github.com/kimtaejin220-dev)
- **Francesco Roberto Terrosu** - [GitHub Profile](https://github.com/FrancescoTerrosu)



