# AI Student Desk Object Sorter
This project uses a web-based tool called Google's Teachable Machine to identify and sort object data found on a typical student desk.

## Classes Identified
* Class 1: Mouse
* Class 2: Pen or Pencil
* Class 3: Sticky Note Pad
* Class 4: Charger
* Class 5: Hand Sanitizer
* Class 6: Stapler

## Discussion & Reflection

1.  **Model Performance & Iteration:**
    * How accurate was your first trained model?
    *    Very accurate, it could identify the items on a clear background with no problem and 90-100% accuracy. It did have some trouble when clutter was introduced, but it still recognized the items.
    *    
    * What steps did you take to iterate and improve its performance? (e.g., added more images, diversified image types for a specific class).
    *    I added as many images as possible for each item and ensured every angle was taken. I also added different variants of some items, such as other mice, chargers, hand sanitizers, and pens and pencils, so it can recognize ones it was not trained on by comparing composition, colors, build, and other similarities.
    *    
    * How did these changes affect the model's accuracy and confidence scores?
    *    It positively affected the model's accuracy. I could show it a random pencil that it was not trained to recognize as a pencil or a pen, and it could still distinguish it. I could also introduce two different items at the same time that it was trained on, and it was able to identify both items in the webcam with a rough 50/50 accuracy.

2.  **Challenges & Observations:**
    * Which objects were the easiest for your model to learn and distinguish? Why do you think that was?
    *    My model was able to recognize chargers, pens or pencils, and the mice the easiest, quickest, and most accurately. This is because all three had the most images the model was trained on; therefore, I concluded that the more images your model has, the more accurate and easier it will be to identify objects.
    *    
    * Which objects were the most challenging? What made them difficult (e.g., similar shapes, variable appearances)?
    *    The objects that it seemed to struggle with the most were the sticky note pad. This is because, from certain angles, it resembles some of the other images for the mouse or hand sanitizer, and the model would get it confused.
    *    
    * What happened when you showed the model an object it wasn't trained on? How did the confidence scores behave, and why is this significant?
    *    It did perfectly fine and was very confident in the object and the score, and was able to distinguish and determine the items. This is significant because training a model to recognize items it hasn't been trained on will help it learn and identify similar items and be confident in the same shape, style, color, and other factors.

3.  **Bias in AI:**
    * If you only trained your "mug" class with images of *your specific mug* (and didn't vary color, shape, etc.), how well do you think it would recognize other students' significantly different mugs? How does this illustrate the concept of bias being introduced through training data?
    *    If you only trained it on your mug and didn't include other options, it may assume that all mugs look like yours, and when it sees something different, it will not be able to accurately or confidently identify it as a mug; therefore, this illustrates bias being introduced because it believes your mug is the only option. Using a variety of mug images, including different colors, shapes, ones with handles, ones without, ones with lids and straws, ones holding liquids, and some empty, will significantly help your model to be able to identify any mug it sees because you included many, if not all, the distinguishing factors.
    *    
    * Imagine all your training images were taken in very bright, direct lighting. What might happen if you tried to use the model in a dimly lit room or with strong shadows? How does this relate to the robustness and potential biases of AI models?
    *    The model was only trained on that direct lighting. If you tried it in a dimly lit room, it may not be able to distinguish the item or factors it needs to identify the object properly. The same applies if the photo is blurry, even though it was trained on clear, distinct images. This relates because without all the factors or values presented, the model will assume that everything it sees will be in direct, clear view. When it is not, it will struggle to identify or not be able to distinguish at all because it is biased towards bright, clear images, rather than blurry, shadowed, or dark images.

4.  **Model Limitations & Usefulness:**
    * What are some key limitations of the model you created?
    *    I didn't have enough variety of certain objects to train my model on a variety of factors or differences in certain items, and therefore, if it was tested on a certain item, it was not trained enough on it, and it may struggle to identify because it didn't have enough data. For example, the sticky note pad and the stapler only have pictures of one item because that was all I had available at the time. In contrast, hand sanitizer has three options, the pen or pencil has like six different options, and the mice and chargers have two. These all have enough or a good amount of variety to confidently distinguish between various items that it was not trained on, if shown. Furthermore, my images were all taken in a brightly lit room with very little clutter, so when introduced to clutter, the model may become overwhelmed. As I mentioned in the questions above, since my model was not trained on different lighting, it may be biased towards dimly lit areas. Additionally, my images were not taken clearly or precisely, so the model may also be confused or biased in those situations.
    *    
    * Why is it useful to be able to download your trained model files (like `model.json`, `weights.bin`) and share them (e.g., via GitHub)? What does this enable?
    *    It's a useful tool that lets you share, deploy, and reuse your trained model so others (or you later if needed) can run it, reproduce or build your results, version it, or integrate it into apps. All without needing to retrain the model again.

5.  **Real-World Applications & Ethics:**
    * Brainstorm 2-3 real-world applications where a similar image classification model could be useful.
    *    A couple of real-world applications where a similar image classification model could be useful are:
    *    Medical imaging — classifying X-rays or skin lesion images to help identify potential diseases.
    *    Security and surveillance — detecting objects like weapons, vehicles, or intruders in camera footage.
    *    Retail inventory management — automatically recognizing products on shelves to track stock levels or detect misplaced items.
    *    
    * Briefly discuss one ethical consideration that developers should keep in mind when building and deploying image recognition AI in the real world (e.g., related to fairness, privacy, misuse).
    *    One key ethical consideration is privacy. Image recognition systems often collect or analyze photos of people who didn’t consent to being recorded. Developers must ensure data is gathered responsibly, stored securely, and used only for its intended purpose to prevent misuse or unauthorized surveillance.

