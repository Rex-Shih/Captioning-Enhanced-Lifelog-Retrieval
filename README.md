# Lifelog Image Caption Dataset for NTCIR-14 Lifelog-3 Lifelog Image Dataset

This repository contains the image captions generated by our method, based on the NTCIR-14 Lifelog-3 lifelog image dataset. The dataset includes various captions generated using different models and methods, providing a comprehensive set of descriptions for each image. The dataset will be made fully available upon acceptance.

## Dataset Description

The dataset is structured as a list of JSON objects, each representing an image with multiple captions generated by different models. Each entry includes:

- **id**: A unique identifier for the image.
- **Idefics2**: Caption generated by the Idefics2 model based on single caption method.
- **LLaVA-Next**: Caption generated by the LLaVA-Next-7B model based on single caption method.
- **Internlm-xcomposer2**: Caption generated by the Internlm-xcomposer2-7B model based on single caption method.
- **Video-LLaVA**: Caption generated by the Video-LLaVA model based on collective caption method.
- **Large-World-Model**: Caption generated by the Large-World-Model based on collective caption method.
- **fine-grained**: Fine-grained caption generated by GPT4-turbo-vision based on merged method.
- **coarse-grained**: Coarse-grained caption generated by GPT4-turbo-vision based on merged method.
- **Experience-summary**: Summary of the experience depicted in the images generated by GPT4-turbo-vision based on merged method.

### Sample Entry

```json
{
    "id": "u1_20180525_0208_i00",
    "Idefics2": "A person is in an elevator that has the number 7 on it.",
    "LLaVA-Next": "The image captures a moment of solitude and introspection in a modern, well-lit elevator. The person, dressed in a crisp white shirt, stands alone, their reflection mirrored in the elevator's polished surface. The elevator's interior is sleek and minimalist, with a blue carpet underfoot and a yellow accent wall adding a pop of color. The time on the elevator reads 07:08, suggesting it's early morning or late evening. The individual appears to be in a state of quiet contemplation, perhaps reflecting on the day ahead or the day just past. The elevator's motion is captured in the blurred background, adding a sense of movement and progress. The overall atmosphere is one of calm and introspection, a snapshot of a moment in time within the confines of an urban elevator.",
    "Internlm-xcomposer2": "The image captures a moment at 07:08, where a person is standing in front of an elevator door. The reflection of the individual can be seen in the mirror-like surface of the door, creating a unique perspective.",
    "Video-LLaVA": "At 07:08, a person is seen holding a knife and cutting a piece of meat. The person is standing in front of a table with a plate of food, and there is a potted plant nearby. The person appears to be focused on their task, and the scene is well-lit, with natural light coming in from a window. The person's actions suggest that they are preparing a meal, and the presence of the potted plant adds a touch of greenery to the setting.",
    "Large-World-Model": "The video showcases a man in a suit entering a luxurious watch store, a woman walking through the store, and a man playing a piano. The man playing the piano is seen from different angles, and the camera pans around the store, capturing the various items on display.",
    "fine-grained": "Blurry reflection of a person in an elevator with visible door frame.",
    "coarse-grained": "Riding the elevator and pressing the floor button.",
    "Experience-summary": "Started the morning by taking the elevator, visiting the hotel lobby, interacting with staff, then enjoying a buffet breakfast."
}
```

## How to Use

1. Clone the repository:
    ```sh
    git clone https://github.com/Rex-Shih/Retrieval-through-Captioning-Enhanced-Interpretation.git
    ```
2. Load the JSON file using your preferred method.


## Contact

For any questions or issues, please open an issue in the repository or contact the author at [yfshih@nlg.csie.ntu.edu.tw].

