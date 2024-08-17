# Character Consistency Experiment

## Purpose

This experiment's goal was to determine if a model could be trained to consistently generate images of a single character across various poses and scenarios. It aimed to achieve a uniform look across images by leveraging fine-tuned image-gen models with Blender CGI.

## Overview

This project was conducted when I was first teaching myself CGI using Blender. The process involved rendering a sequence of images (typically PNG files) in Blender, which were then compiled into an animation using video editing software.

### Steps Involved

1. **Character Design & Dataset Creation**:
    - Collaborated with a local artist to create a large dataset of hand-drawn character images in various positions.
    - Scanned the drawings, removed the background, and ensured the colors were consistent with the CGI character.
    - Recreated the character in Blender, matching the CGI puppet with the artist's drawings.

2. **Model Training**:
    - Used the [EveryDream 2 trainer](https://github.com/victorchall/EveryDream2trainer) to fine-tune an image generation model from Hugging Face.
    - Incorporated both the hand-drawn and CGI images into the training process.
    - Generated additional images of the character and added them to the dataset for further training.

3. **Animation Creation**:
    - Rendered two animation examples: a close-up and a walking shot, showcasing the character's movement.
    - Compiled these animations using the Fusion page within DaVinci Resolve, applying filters to ensure consistent animation quality.

### Results

- The character's consistency across images improved, though the model struggled with variations or anything outside of the training data.
- The model occasionally hallucinated new colors, introducing inaccuracies, such as a red body instead of a brown one in certain outputs.

### Lessons Learned

- **Consistency vs. Flexibility**: While the character's appearance remained consistent, the model's ability to generalize was limited. A more general-purpose training set could provide better results by accommodating variations and gaps in the training data.
- **Modern Methodologies**: With today's tools, separating and training on a character has become more straightforward, eliminating the need for some of the earlier steps.

## Accessing Project Files

Due to the large file sizes, the project files, including input and output copies of the image experiment, the Blender model for the bird, the trained model itself, and the final animation in .mov format are hosted on Google Drive. You can access all related files here:

- [Google Drive Link](https://drive.google.com/drive/folders/1bMEn9NmzAow0c91inD7OWla-HsNH06vA?usp=sharing)

## Recreating This Project

To replicate this experiment, you can use the links below for the EveryDream Trainer and Hugging Face models:

- [EveryDream 2 Trainer on GitHub](https://github.com/victorchall/EveryDream2trainer)
- [Hugging Face Image Generation Models](https://huggingface.co/models)

You can choose any image-generation model from Hugging Face that suits your needs.

## Future Improvements

If I were to redo this experiment, I would explore several advanced techniques and methodologies to further refine and expand the scope of the project:

### 1. **Incorporating Motion Capture for Blender Models**

One potential enhancement is integrating motion capture technology with the Blender model. Since experiments with AI animation often involve people using videos of themselves and turning them into something else, I want to try to add an extra layer to that process. Take a video of yourself, use motion capture tech to put that onto a loosely designed model of what you want the final result to look like, and then process that into the final animation rendering using Img2Img. Applying motion capture data to the CGI character could make the movement more natural and realistic, while adding in the CGI translation layer will give you more control over the data being processed into the final result, creating a more cohesive and seamless animation.

### 2. **Experimenting with Unreal Engine 5’s MetaHuman**

Another exciting avenue for exploration involves using Unreal Engine 5’s MetaHuman framework. This tool could be leveraged to create hyper-realistic digital humans, which could then be translated into images that mimic the appearance of a real person. By training the model on these MetaHuman-generated images, it would be possible to explore how well the model can maintain consistency when working with more lifelike characters. This would not only test the model's ability to handle realistic textures and features but also push the boundaries of character consistency in image generation.

### 3. **Exploring Advanced Image Isolation Techniques**

With advancements in image processing technologies, new isolation methods could be employed better to separate the character from the background and other elements. Modern techniques, such as semantic segmentation or neural network-based background removal, could provide more accurate and detailed isolation of the character in each frame. Using these techniques, the training data could be enhanced with cleaner, more precise images, leading to improved animation guidance and more consistent output. These methods could also allow for better handling of lighting, shading, and perspective variations, further refining the model’s performance.

### 4. **Utilizing Expanded Data for Animation Guidance**

In conjunction with the above techniques, incorporating a broader dataset that includes diverse scenarios, lighting conditions, and character poses could significantly enhance the model's robustness. By guiding the animation with richer data, the model would be better equipped to handle variations and produce high-quality, consistent results across a wider range of conditions. This expanded dataset would also provide a more comprehensive training experience, allowing the model to learn and adapt to different contexts more effectively.

By implementing these improvements, the experiment could yield more sophisticated and versatile results, pushing the limits of what’s possible with character consistency in image generation.

## View the Results

You can view the final animation in the .mov file included in the Google Drive link above.

## Acknowledgments

- **Artist**: Thank you Oliver for providing the hand-drawn character dataset.
- **Tools Used**: Blender, Hugging Face, [EveryDream 2](https://github.com/victorchall/EveryDream2trainer), DaVinci Resolve
