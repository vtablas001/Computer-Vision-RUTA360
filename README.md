
# RUTA360: Computer Vision Prototype for Tourism Intelligence in El Salvador

**RUTA360** is an AI-powered computer vision prototype I designed to provide real-time tourism intelligence in public spaces and natural parks across El Salvador. By using YOLOv8 and outdoor IP cameras, this solution aims to track visitor flow, identify crowding patterns, and support data-driven decision-making for institutions such as MITUR and ISTU.

<img width="1915" height="896" alt="image" src="https://github.com/user-attachments/assets/e7e1f507-de31-40f6-bfec-bf0d8cef2037" />

- [Ruta 360 demo](https://v0-ruta360-computer-vision.vercel.app/)

##  Executive Summary

El Salvador's parks and urban spaces are witnessing a steady increase in tourism, yet current monitoring tools fall short in capturing real-time visitor dynamics. RUTA360 bridges that gap using AI-based detection and tracking, enabling smarter planning, infrastructure optimization, and safer tourist experiences.

##  Context

Places like Balboa Park, El Boquerón, Historic Downtown, and Cerro Verde face:
- Overcrowding in peak hours
- Underused infrastructure
- Limited real-time visitor data

Traditional methods (manual counts, periodic estimates) are insufficient for dynamic management. RUTA360 introduces AI and computer vision to detect:
- Movement and behavior within parks
- Real-time crowding
- Infrastructure usage patterns

<img width="1260" height="717" alt="image" src="https://github.com/user-attachments/assets/bfadb5c8-dd40-4bb3-bdf3-5fd1e434e481" />


##  Tech Stack

**Core Libraries & Tools**

[![Python](https://img.shields.io/badge/Python-3776AB?logo=python&logoColor=white)](https://www.python.org/)
[![YOLOv8 by Ultralytics](https://img.shields.io/badge/YOLOv8-Ultralytics-green)](https://docs.ultralytics.com/)
[![OpenCV](https://img.shields.io/badge/OpenCV-5C3EE8?logo=opencv&logoColor=white)](https://opencv.org/)
[![Roboflow](https://img.shields.io/badge/Roboflow-0A0A0A?logo=roboflow&logoColor=white)](https://roboflow.com/)
[![Power BI](https://img.shields.io/badge/Power%20BI-F2C811?logo=powerbi&logoColor=black)](https://powerbi.microsoft.com/)
[![Google Colab](https://img.shields.io/badge/Google%20Colab-F9AB00?logo=google-colab&logoColor=white)](https://colab.research.google.com/)

**Hardware Components**
- [LUCID Vision Labs Triton IP67 Camera](https://thinklucid.com/) are Roboflow recommendations
- Edge Computing Device (Jetson Orin)
- 6m galvanized poles
- Solar/battery-powered outdoor setups
- Optional stereo vision for 3D mapping

##  Key Tourism Metrics

| Metric                         | Description |
|-------------------------------|-------------|
| Visitor Counts                | Per hour, per day, per entrance |
| Heatmaps                      | Most and least visited areas |
| Dwell Time                    | At scenic spots, lookouts, food courts |
| Flow Patterns                 | Trail usage, bottlenecks, peak hours |
| Parking Usage                 | Vehicle tracking, overflow management |
| Group Composition             | Solo vs group/family travelers |
| Visit Duration                | Quick stops vs full-day engagement |
| Infrastructure Utilization    | Bathrooms, picnic zones, soccer fields |
| Real-Time Congestion Alerts   | Safety & crowd control |

##  Hypotheses to Validate

- If shaded areas correlate with longer dwell time → improve rest zones.
- If entry peaks differ between weekdays vs weekends → optimize staffing.
- If real-time congestion detected → activate overflow strategies or reroute.
- If trail usage is low → evaluate signage/accessibility.

##  How It Works

### 1. Data Capture
- Drone or static camera footage
- Annotate using Roboflow or MakeSense.ai

### 2. Model Setup
- YOLOv8 pretrained on COCO dataset
- Fine-tune on local data (optional)
- Run inference with BoT-SORT for tracking

### 3. Deployment
- Install cameras and solar power systems
- Configure detection + tracking pipelines
- Store metrics in local/cloud databases

### 4. 📈 Dashboarding
- BI dashboards for institution such as MITUR and ISTU
- Daily/weekly reports and alerts

## Ethics, Privacy & Sustainability

-  No facial recognition or PII collected
-  GDPR-aligned privacy practices
-  Solar-powered and environmentally sustainable
-  Tamper-proof installations

## Prototype Roadmap

1.  Initial video-based pilot
2.  Model tuning + validation
3.  Real-world camera installation
4.  Dashboard development
5.  Hypothesis testing & insights

##  Scaling & Governance

- **Institutional Hosting**: MITUR, ISTU or municipalities
- **Funding**: National tourism budgets + IDB/CAF/BCIE grants
- **Maintenance**: Public-private partnerships for ops support

##  Risks & Mitigation

| Risk                         | Likelihood | Mitigation |
|-----------------------------|------------|------------|
| Camera vandalism            | Medium     | Community ownership + secure mounts |
| Network loss                | High       | Offline sync + solar backup |
| Privacy concerns            | Medium     | Transparency + blurred faces |
| Low-light detection failure | Medium     | Camera placement + fine-tuning |

##  Sample YOLOv8 Configuration

```python
from ultralytics import YOLO

model = YOLO("yolov8n.pt")
results = model("demo_video.mp4", stream=True, conf=0.4)
```

##  Contact

**Víctor A. Tablas**  
victor.tablas@gmail.com
[LinkedIn](https://www.linkedin.com/in/victor-tablas/)

## License

This project is licensed under the [MIT License](LICENSE).
