# Enhanced-YOLOv11-EgoHands-Detection
## 📌 Overview
Enhancing the fidelity of human-computer interaction requires accurate and real-time hand detection, particularly from first-person egocentric perspectives. 

This repository presents an enhanced version of YOLOv11, a customized hand detection framework designed for egocentric visual input captured from head-mounted displays.

The system detects and classifies four hand categories:
- myleft  
- myright  
- yourleft  
- yourright
   
## 🚀 Key Contributions

- Replacement of standard Conv layers with GhostConv in layers 3 and 7
- Improved computational efficiency without sacrificing accuracy
- Perspective-aware multi-class hand detection
- Real-time inference performance

## 📊 Dataset

The model was trained and evaluated on the EgoHands dataset, which contains complex hand-object interactions under varied environmental conditions.

## 📈 Performance Results

| Metric        | Value |
|--------------|--------|
| Precision    | 98%   |
| Recall       | 97%   |
| F1-score     | 97%   |
| mAP@50       | 99%   |
| FPS          | 204   |
| Latency      | 4.9 ms |

### Performance Improvement Over Standard YOLOv11

- +12.21% increase in inference speed  
- −10.91% reduction in latency  

The proposed model establishes a new benchmark in efficiency and effectiveness for egocentric hand detection.

## 🧠 Model Architecture
![Model Architecture](Yolov11n.png)

Ghost Convolution (GhostConv) layers were integrated into YOLOv11 to reduce feature redundancy and improve computational efficiency.




📄 Citation

If you use this work, please cite:
@INPROCEEDINGS{11315447,
  author={Nahar, Aminun and Shuvo, Mehedi Hasan and Islam, Mahbubul and Anannya, Rifat Tasnim and Parvin, Shahnaj and Nur, Kamruddin},
  booktitle={2025 IEEE/ACS 22nd International Conference on Computer Systems and Applications (AICCSA)}, 
  title={Deep Learning Based Real-Time Hand Detection Using First-Person Egocentric Perspectives}, 
  year={2025},
  volume={},
  number={},
  pages={1-5},
  keywords={Hands;Deep learning;Visualization;Accuracy;Head-mounted displays;Computational modeling;Redundancy;Object detection;Real-time systems;Standards;Egocentric Vision;hand detection;hand classification;real-time Object Detection;deep learning;YOLOv11},
  doi={10.1109/AICCSA66935.2025.11315447}}
