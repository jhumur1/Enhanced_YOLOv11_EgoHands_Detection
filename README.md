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
Training set: 3840 images

Validation set: 480 images
The dataset is available on Roboflow:

[Hands-LR34x Dataset (Roboflow)](https://app.roboflow.com/american-international-university-bangladesh-iyfmc/hands-lr34x/models)

📝 Data Preprocessing & Annotation
Annotation Tool: Roboflow

Steps performed:

Uploaded raw EgoHands dataset to Roboflow workspace.

Annotated bounding boxes for hands (4 classes).

Applied preprocessing: resizing to 640×640, Auto-Orient and Resize.

Exported dataset in YOLOv11 format.

Advantages: Roboflow ensured clean labels, consistent formatting, and easy integration with Ultralytics YOLO.

Methodology:

The experiments were conducted using Google Colab, which provided 12.7 GB of RAM, a Tesla T4 GPU with 15 GB of memory, and approximately 70 GB of free storage. The runtime environment was Python 3.11.13. The software stack included Keras/TensorFlow, Ultralytics YOLO v8.3.155, and PyTorch 2.6.0.

Each model was trained for 70 epochs to ensure sufficient learning of the dataset’s complexity. A batch size of 12 was selected due to GPU memory constraints, while depth and width scaling factors were set to 0.5 to reduce model size and memory usage without sacrificing accuracy. The confidence threshold was fixed at 0.5 to balance precision and recall, and the IoU threshold was set at 0.7 to enforce stricter localization. Training employed the AdamW optimizer with a learning rate of 0.00125. All input images were resized to 640×640 pixels to maintain consistency across models.

The proposed YOLOv11n model consists of 185 layers, 5.63 million parameters, and requires 17.5 GFLOPs per forward pass.


## 🧠 Model Architecture
![Model Architecture](Yolov11n.png)

Ghost Convolution (GhostConv) layers were integrated into YOLOv11 to reduce feature redundancy and improve computational efficiency.

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
