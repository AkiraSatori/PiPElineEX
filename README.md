# PiPElineEX
Source code of our paper "A pipeline-based approach for automated construction of geoscientific knowledge graphs.(editing)"

## Overview
This file contains detailed code for the automation module, excluding the pre-trained models.

In our work, we propose an automated knowledge graph construction program method,it can improve the efficiency of knowledge graph construction to shorten the development process.

We divide the construction of the geoscientific knowledge graph into several functional modules, which can be tailored to meet the varying needs of different users by modifying the module design.

Please find more details of this work in our paper


### Dependencies
```
scikit-learn==1.1.3
scipy==1.10.1
seqeval==1.2.2
pytorch-crf==0.7.2
py2neo
transformers
```

### Directory Structure
```
PipeLineEX/
├── checkpoint/
│   ├── saved model
├── data/
│   ├── ner_data/
│   │   ├──Annotated ner-Data(train.txt)
│   │   ├──Annotated ner-Data(dev.txt)
│   │   └──Annotated ner-Data(labels.txt)# Entity Types
│   └── re_data/
│   │   ├──Annotated re-Data(train.txt)
│   │   ├──Annotated re-Data(dev.txt)
│   │   ├──Annotated re-Data(labels.txt)
│   │   └──Annotated ner-Data(rels.txt) # Relationship Types between Entities
├── model-hub # pretrained model
├── _init_.py
├── combine.py # Node merge
├── config.py # model train config
├── data_loader.py 
├── genjson.py # Annotated data transfer
├── Kgraph.py  
├── model.py 
├── predict.py 
├── pdftotxt.py 
├── ner_main.py
├── re_main.py
└── run_main.py
```

### START
Run this program
```
python run_main.py
```

### Extension

There are some issues with relation extraction, such as the inability to distinguish multiple relationships between two entities and the inability to effectively identify relationships between similar entities. 

All of these problems can be effectively addressed by modifying the knowledge extraction framework.
