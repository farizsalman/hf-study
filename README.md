Libraries and Versions :
    transformers version: 5.12.1
    datasets version: 5.0.0
    evaluate version: 0.4.6
    gradio version: 6.19.0
    accelerate version: 1.14.0
    huggingface_hub version: 1.20.1
    peft version: 0.19.1





TOPICS :

-INFERENCE : Using trained models to generate output or make predictions based on new input data
-SST 2 (Stanford Sentiment Treebank 2): It is a sentiment analysis dataset used to train and evaluate NLP models
-Downstream Task : Finetuning for one specific task
-Biased Prediction: A model is biased if it tends to make systematically different or unfair predictions for certain groups of people.
- Parameter: They are the values the model learns during training.









EXPLORING MODELS:

    Text generation:
        1.Model = zai-org/GLM-5.2 
         purpose = Long horizon task (Horizon task = task that requires an Ai system to plan and work toward one goal over many steps, making decisions along the way.)
         1M token context

    Image-Text to Image:
        1. Model = nomadoor/flux-2-klein-9B-schematic-lora
           Purpose = Takes and image and text as input, and generate a new image as output based on the given reference.

    Text to Image Diffusion model:
        1. Model = krea/Krea-2-Turbo
           Pupose = generate image from text through diffusion
           












Different Type of Tasks done by models

| Task                | What the model predicts                             |
| ------------------- | --------------------------------------------------- |
| Relative Depth      | Which objects are closer or farther away            |
| Surface Normal      | Which direction each surface is facing              |
| Body Pose           | Positions of the main body joints                   |
| Full Pose           | Positions of body, hands, and face joints           |
| Binary Segmentation | Which pixels belong to the object vs. background    |
| Amodal Segmentation | The full shape of an object, including hidden parts |





MODEL CARDS :

    Model name: distilbert/distilbert-base-uncased-finetuned-sst-2-english
        DESCRIPTION:
            - text classification
            - Fine tuned on DistilBert
            - For sentiment analysis
        TRAINING DATA:
            - dataset: Stanford Sentiment treebank 2
            - Binary (Positive & Negative) 
        EVALUATION:
            - Accuracy is 91.3 on dev set
        INTENDED USES:
            - Text classification
            - masked language modeling or next sentence prediction
        LIMITATIONS & BIAS:
            - model could produce biased predictions that target underrepresented populations
            - Biased result based on the country.
    

    Model name: mistralai/Mistral-7B-Instruct-v0.1
        DESCRIPTION:
            - 7 Billion Parameters
            -  It is an Instruction trained model
            - Model Architecture: Grouped-Query Attention, Sliding-Window Attention, Byte-fallback BPE tokenizer
        TRAINING DATA: 
            - Dataset: Publicily available coversation datasets
        INTENDED USE :
            - Text generation, General conversation
            - Instruction following, Summarization
        LIMITATIONS & BIAS:
            - It is mainly a demonstration of instruction tuning
            - It may generate offensive content because it does not have any moderation mechanism
    
    Model name: google/mt5-base
        DESCRIPTION:
            - It is a base model
            - Trained on 101 languages
        TRAINING DATA:
            - Dataset: mC4
            - 
        INTENDED USE:
            - Text to text generation
        LIMITATION & BIAS:
            - Base model, need to be finetuned if needed for any specific task
