# Visual Lifelog Retrieval through Captioning-Enhanced Interpretation (CIVIL)

This repository releases the **caption dataset** and supporting resources for our **IEEE BigData 2024** paper, **“Visual Lifelog Retrieval through Captioning-Enhanced Interpretation (CIVIL)”**. The core idea is **captioning before retrieval**. We generate multiple caption types per image (and per short sequence), then retrieve with text–text similarity.

---

## 🔗 Paper

- **Preprint (PDF):** [paper.pdf](paper.pdf)  
- **IEEE Xplore:** https://ieeexplore.ieee.org/document/10825835
> © 2024 IEEE. Personal use of this material is permitted. Permission from IEEE must be obtained for all other uses, including reprinting/republishing this material for advertising or promotional purposes, creating new collective works, for resale or redistribution to servers or lists, or reuse of any copyrighted component of this work in other works. Published in 2024 IEEE International Conference on Big Data (BigData). DOI: 10.1109/BigData62323.2024.10825835


---

## 📦 Dataset Access

**➡️ Download (Google Drive):** https://drive.google.com/file/d/1L8RDqUijk9KOgylwxpFGmOUM-mmuqNpN/view?usp=sharing  

---

## 🧾 JSON Format (exact field names)

Each JSON object contains **only captions** (no original dataset metadata). Field names are as below:

- `id`  
- `Idefics2`  
- `LLaVA-Next`  
- `Internlm-xcomposer2`  
- `Video-LLaVA`  
- `Large-World-Model`  
- `fine-grained`  
- `coarse-grained`  
- `Experience-summary`

### Sample Entry
Also see [sampleData.json](sampleData.json)  
```json
{
  "id": "u1_20180525_0208_i00",
  "Idefics2": "A person is in an elevator that has the number 7 on it.",
  "LLaVA-Next": "The image captures a moment of solitude and introspection in a modern, well-lit elevator. The person, dressed in a crisp white shirt, stands alone, their reflection mirrored in the elevator's polished surface. The elevator's interior is sleek and minimalist, with a blue carpet underfoot and a yellow accent wall adding a pop of color. The time on the elevator reads 07:08, suggesting it's early morning or late evening. The individual appears to be in a state of quiet contemplation, perhaps reflecting on the day ahead or the day just past. The elevator's motion is captured in the blurred background, adding a sense of movement and progress. The overall atmosphere is one of calm and introspection, a snapshot of a moment in time within the confines of an urban elevator. ",
  "Internlm-xcomposer2": "The image captures a moment at 07:08, where a person is standing in front of an elevator door. The reflection of the individual can be seen in the mirror-like surface of the door, creating a unique perspective.",
  "Video-LLaVA": "At 07:08, a person is seen holding a knife and cutting a piece of meat. The person is standing in front of a table with a plate of food, and there is a potted plant nearby. The person appears to be focused on their task, and the scene is well-lit, with natural light coming in from a window. The person's actions suggest that they are preparing a meal, and the presence of the potted plant adds a touch of greenery to the setting.",
  "Large-World-Model": "The video showcases a man in a suit entering a luxurious watch store, a woman walking through the store, and a man playing a piano. The man playing the piano is seen from different angles, and the camera pans around the store, capturing the various items on display.",
  "fine-grained": "Blurry reflection of a person in an elevator with visible door frame.",
  "coarse-grained": "Riding the elevator and pressing the floor button.",
  "Experience-summary": "Started the morning by taking the elevator, visiting the hotel lobby, interacting with staff, then enjoying a buffet breakfast."
}
```

---

## 🔒 Licensing & Usage

- These captions are released for **research** use.  
- The original lifelog images belong to **NTCIR-14 Lifelog-3**—please obtain and follow their license.  
- When publishing results, cite our paper (BibTeX below) and **credit Lifelog-3**.
- Original lifelog images are NOT included and require NTCIR-14 Lifelog-3 access per their user agreement.

---

## ✍️ Citation (BibTeX)

```bibtex
@INPROCEEDINGS{10825835,
  author={Shih, Yu-Fei and Yen, An-Zi and Huang, Hen-Hsen and Chen, Hsin-Hsi},
  booktitle={2024 IEEE International Conference on Big Data (BigData)}, 
  title={Visual Lifelog Retrieval through Captioning-Enhanced Interpretation}, 
  year={2024},
  volume={},
  number={},
  pages={479-486},
  keywords={Visualization;Big Data;Cameras;Vectors;Image reconstruction;Lifelogging;Visual Lifelog Captioning;Visual Lifelog Retrieval},
  doi={10.1109/BigData62323.2024.10825835}}
```

---

## 📬 Contact

Open a GitHub issue or email **ys7237@nyu.edu**.
