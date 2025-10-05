**Canonical dataset home (lab):** https://github.com/ntunlplab/Visual-Lifelog-Retrieval-through-Captioning-Enhanced-Interpretation  
**Personal mirror & paper companion:** this repo.

# Visual Lifelog Retrieval through Captioning-Enhanced Interpretation (CIVIL)

This repository hosts the **caption dataset metadata** and paper resources for our **IEEE BigData 2024** paper, **“Visual Lifelog Retrieval through Captioning-Enhanced Interpretation (CIVIL)”**.  
Core idea: **caption first, retrieve later**. We generate multiple caption types per image (and short sequence), then retrieve via text–text similarity.


---

## Paper

- **Preprint (PDF):** [paper.pdf](paper.pdf)  
- **IEEE Xplore:** https://ieeexplore.ieee.org/document/10825835

> © 2024 IEEE. Personal use permitted. For all other uses (reprint/republish/ads, resale/redistribution, etc.), obtain permission from IEEE. Published in 2024 IEEE International Conference on Big Data (BigData). DOI: 10.1109/BigData62323.2024.10825835

---

## Dataset Access

**Download (Google Drive):** https://drive.google.com/file/d/1L8RDqUijk9KOgylwxpFGmOUM-mmuqNpN/view?usp=sharing

This archive contains **captions only** (no images). Original lifelog images belong to **NTCIR-14 Lifelog-3** and require separate access (see Licensing & Usage).

---

## JSON Format

Each JSON object contains **only captions** (no original lifelog images or their metadata).  
Top-level keys include model-specific captions plus a nested `GPT4-0613` object:

- `id`  
- `Idefics2`  
- `LLaVA-Next`  
- `Internlm-xcomposer2`  
- `Video-LLaVA`  
- `Large-World-Model`  
- `GPT4-0613` *(object)*  
  - `fine-grained`  
  - `coarse-grained`  
  - `Experience-summary`

### Sample Entry
```json
"../imageData/2018_05_03/B00001382_21I6X0_20180503_072333E.JPG": {
  "id": "u1_20180503_0617_i01",
  "Idefics2": "A person is holding a keyboard and water bottle.",
  "LLaVA-Next": "The image captures a moment of quiet solitude, as a person sits in a room, engrossed in the digital world. The individual, clad in a vibrant red sweater, is holding a smartphone in their hands, their fingers dancing over the screen. The phone is connected to a laptop, suggesting a work or study session in progress.\n\nThe room around them is a testament to their lifestyle, with a desk and a chair visible in the background. A backpack rests on the floor, perhaps holding more tools of their trade. A water bottle stands nearby, a silent reminder of the importance of hydration amidst long hours of screen time.\n\nThe time on the phone reads 06:17, hinting at the early morning hours. The person seems to be in the midst of a productive session, perhaps working on a project or studying for an exam. The image paints a picture of modern life, where technology plays a significant role in our daily routines.",
  "Internlm-xcomposer2": "At 06:17, a person is in their living room, holding a smartphone with a white cord attached to it. They are wearing a red sweater and a watch on their wrist.",
  "Video-LLaVA": "At 06:17, a person is holding a large piece of meat, which is wrapped in plastic. The meat appears to be a type of salmon, and the person is holding it up to the camera. The person is standing in a kitchen, and there are several other items visible in the background, including a sink, a refrigerator, and a microwave. The person seems to be proudly displaying the meat, possibly showcasing its size or quality.",
  "Large-World-Model": "The video shows a person using a toaster oven to make coffee. They place a cup of coffee on a plate and close the toaster oven. Then, they open the door of the oven and place a plate of food in it. The video also shows a hand holding a cup of coffee in a kitchen.",
  "GPT4-0613": {
    "fine-grained": "Person holding a cellphone with a charging cable connected.",
    "coarse-grained": "Morning routine in a residential setting, involving smartphone usage and preparing smoked salmon in the kitchen.",
    "Experience-summary": "The individual started their morning by handling their phone and preparing smoked salmon in a well-lit kitchen."
  }
}
```
## Quickstart (load + inspect)

```python
import json, pathlib

# Path to your captions JSON (after extracting from the Drive archive)
p = pathlib.Path("captions.json")  # replace with actual filename

data = json.loads(p.read_text())

# Get the first entry
first_key, first_val = next(iter(data.items()))
print("Path key:", first_key)
print("ID:", first_val["id"])

# Access a model caption
print("Idefics2:", first_val.get("Idefics2", ""))

# Access GPT4-0613 structured fields
gpt4 = first_val.get("GPT4-0613", {})
print("fine-grained:", gpt4.get("fine-grained", ""))
print("coarse-grained:", gpt4.get("coarse-grained", ""))
print("Experience-summary:", gpt4.get("Experience-summary", ""))
```
---

## Licensing & Usage

- Captions are released for **research** use.  
- The original lifelog images belong to **NTCIR-14 Lifelog-3**. You must obtain access and comply with their license and user agreement.  
- The dataset here **does not** include original images.  
- When publishing results, please cite our paper (BibTeX below) and **credit NTCIR-14 Lifelog-3**.

---

## Citation (BibTeX)

```bibtex
@INPROCEEDINGS{10825835,
  author={Shih, Yu-Fei and Yen, An-Zi and Huang, Hen-Hsen and Chen, Hsin-Hsi},
  booktitle={2024 IEEE International Conference on Big Data (BigData)},
  title={Visual Lifelog Retrieval through Captioning-Enhanced Interpretation},
  year={2024},
  pages={479-486},
  keywords={Visualization;Big Data;Cameras;Vectors;Image reconstruction;Lifelogging;Visual Lifelog Captioning;Visual Lifelog Retrieval},
  doi={10.1109/BigData62323.2024.10825835}
}
```

---

## Contact

Open a GitHub issue or email **ys7237@nyu.edu**.
