# Entity_Classification_in_Memes
- Classifies entity present in a meme into hero', villain', victim' or other' based on OCR and image features, using CLIP models 
combined with BERT embedding.
- Maximized macro F1 score through hyperparameter tuning and finding best combination of 
CLIP model and end classifier.

## Description of Research Problem
The description of the research problem/competition is available here: https://codalab.lisn.upsaclay.fr/competitions/906#learn_the_details-overview
Also, the necessary details needed to understand the project is available as follows:

- The CONSTRAINT-2022 shared task on the topic "Hero, Villain and Victim: Dissecting harmful memes for Semantic role labelling of entities" invites participation in the following task, Role labeling for memes: The second subtask emphasizes detecting which entities are glorified, vilified or victimized, within a meme. Assuming the frame of reference as the meme author's perspective, the objective is to classify for a given pair of a meme and an entity, whether the entity is being referenced as Hero vs. Villain vs. Victim vs. Other, within that meme.
  
- Dataset Links: This is the data for the competition. It is to be used responsibly.
The train/val set for Covid-19 domain can be downloaded from this link
The train/val set for US Politics domain can be downloaded from this link

- Shared Task: Hero, Villain and Victim: Dissecting harmful memes for Semantic role labelling of entities
Definition: Given a meme and an entity, determine the role* of the entity in the meme: hero vs. villain vs. victim vs. other.
*The meme is to be analyzed from the perspective of the author of the meme

- Definition of the Entity Classes
Hero: The entity is presented in a positive light Glorified for their actions conveyed via the meme or gathered from background context
Villain: The entity is portrayed negatively, e.g., in an association with adverse traits like wickedness, cruelty, hypocrisy, etc. 
Victim: The entity is portrayed as suffering the negative impact of someone else’s actions or conveyed implicitly within the meme.
Other: The entity is not a hero, a villain, or a victim.


- Unseen Test Set: The “unseen test set” file and the corresponding image set will have samples from both Covid-19 and the US Politics domain.

File format:

{‘image’ : memes_1486.png’,‘OCR’: "AAE RNC\nCONVENTION 2020:\nHOPEAND\nPOSITIVITY\nDNC CONVENTION 2020:\nDOOM AND GLOOM\n",‘entity_list’ :['Donald Trump', 'Joe Biden','Democratic National Convention (DNC)’, 'Republican National Convention (RNC)']}
<img width="873" alt="image" src="https://github.com/Esshaan-Mahajan/Entity_Classification_in_Memes/assets/56061481/5aad7804-5f8c-4ce9-baa3-27ee67542123">

{‘image’ : ‘image_2.png’,‘OCR’ : "Whole world to\nPutin:\n*Putin\nVaccine\nWell done putin. I'm so proud of you\nVaccine\nVaccine\n",‘entity_list’ : [‘Vladimir Putin’, ‘the world’, ‘Salman Khan’, ‘vaccine’]}
<img width="884" alt="image" src="https://github.com/Esshaan-Mahajan/Entity_Classification_in_Memes/assets/56061481/d367bba3-85bb-4c30-98ac-ebdc8342f2b3">



- Submission File format:

{‘image’ : memes_1486.png’, ‘hero’ :['Donald Trump'], ‘villain’ : ['Joe Biden'], ‘victim’ : [], ‘other’ : ['Democratic National Convention (DNC)’, 'Republican National Convention (RNC)']}

{‘image’ : ‘image_2.png’, ‘hero’ : [‘Vladimir Putin’], ‘villain’ : [], ‘victim’ : [], ‘other’ : [‘the world’, ‘Salman Khan’, ‘vaccine’]}

- Evaluation Criteria: The official evaluation measure for the shared task is the "macro" F1 score for the multi-class classification. The evaluation will be done at the corpus level and not at the sample (meme) level. 

**Please note, the evaluation of the submissions will be done on an unseen test set, that is a combination of data from both "Covid-19" and "US Politics".
Note: This work was done by me as research intern at IIITD.

## Related Data
The files related to the project used by me are present here: https://drive.google.com/drive/folders/1VzxEFNfLCDZr6FxFo6Obwzp3iY1F6hol?usp=sharing
## Other Useful links used for development and research
- https://viso.ai/deep-learning/mask-r-cnn/#:~:text=Mask%20R%2DCNN%2C%20or%20Mask,image%20segmentation%20and%20instance%20segmentation.&text=The%20computer%20vision%20task%20Image,also%20known%20as%20image%20objects).
- https://github.com/NVlabs/SCOPS
- http://densepose.org/#:~:text=Dense%20human%20pose%20estimation%20aims,surface%20of%20the%20human%20body.&text=We%20propose%20DensePose%2DRCNN%2C%20a,at%20multiple%20frames%20per%20second.
- https://github.com/facebookresearch/detectron2/tree/main/projects/DensePose
- https://www.kaggle.com/code/cdeotte/pseudo-labeling-qda-0-969/notebook
- https://openai.com/research/clip#fn3
- https://arxiv.org/abs/2103.00020
- https://github.com/openai/CLIP/blob/main/clip/model.py
- https://huggingface.co/docs/transformers/model_doc/convbert
- https://deeplobe.ai/image-segmentation/
- https://paperswithcode.com/methods/category/image-models
