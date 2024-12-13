Dataset：
------
  
coco_butd and f30k_butd: Datasets used for the Faster-RCNN image backbone. We use the pre-computed features provided by SCAN, which can be downloaded via https://github.com/kuanghuei/SCAN#download-data.
All datasets used in the experiments are organized in the following manner:  
```
data  
├── coco  
│   ├── precomp  # pre-computed BUTD region features for COCO, provided by SCAN  
│   │      ├── train_ids.txt  
│   │      ├── train_caps.txt  
│   │      ├── ......  
│   │  
│   ├── images   # raw coco images  
│        ├── train2014  
│        └── val2014  
│    
├── f30k  
│   ├── precomp  # pre-computed BUTD region features for Flickr30K, provided by SCAN  
│   │      ├── train_ids.txt  
│   │      ├── train_caps.txt  
│   │      ├── ......  
│   │  
│   ├── flickr30k-images   # raw coco images  
│          ├── xxx.jpg  
│          └── ...  
│     
└── vocab  # vocab files provided by SCAN (only used when the text backbone is BiGRU)   
```

Training and Evaluation：
------

Training on the Flicker30K or COCO dataset:
1. Switch to the shell folder in the corresponding path. For example:
  ```
  cd ./ELSE_BIGRU/sh
  ```
2. run ./train_xxx_f30k.sh or ./train_xxx_coco.sh. For example:
  ```
  sh train_GRU_f30k.sh
  ```
