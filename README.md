# ProdMatch

## Team Member: Chen Wang, Jiaguan Tang, Bocheng Zhang, Yue Lan

### Introduction
In today's digital marketplace, users face a daunting challenge: sifting through an overwhelming array of products to find ones that genuinely meet their needs. While traditional recommendation systems rely on keyword-based searches and collaborative filtering, these methods often fail to understand nuanced user preferences and context. The rise of multi-modal systems offers a transformative opportunity to bridge this gap. 

ProdMatch aims to revolutionize product discovery by leveraging LMMs to interpret complex user queries and product descriptions, delivering recommendations that go beyond superficial keyword matches. This project seeks to transform e-commerce by addressing limitations in existing systems and enhancing the user experience with precise, personalized, and intent-driven product suggestions. By combining textual and visual data, ProdMatch envisions a solution that reflects true user intent, making product search intuitive and effective. 

### Navigation
+ "InternVL-main" folder contains our model(baseline and finetuned)
+ "code" folder contains all relative code
+ "Json" folder contains the structured dataset
+ "rawData" folder contains the original dataset
+ "test" folder contains the testing set
+ **"\code\internvl_sft.ipynb" contains the finetuning process**
+ **"pipeline.ipynb" contains the complete recommendation pipeline**
### Result
All models we used are run on google Colab using an A100 graphic. A result table is shown below:

![195db125912e0b457fd6f88dcf7be94](https://github.com/user-attachments/assets/45fc4dc1-de95-437b-959f-897094126c71)

### Model Source
We used the InterVL-8b multimodal model for this task. A GitHub link is attached for reference: https://github.com/OpenGVLab/InternVL

### Pipeline Introduction
We create an pipeline.ipynb which including two use cases:
1. New Product Upload: Using InterVL-8b analys the feature from input figure and product description. The model will return the JSON file with price, length, width, height, color. Then we use this information upload the product to product_database.csv.
2. User Query Matching: Using InterVL-8b analys the feature from input query. The system will return top-5-match-product information.
