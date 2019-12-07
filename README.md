
## Directory structure
```
├── TrashNet-Overlap-Collage
│   ├── Split
│   │   ├── test_set
│   │   ├── train_set
│   │   └── val_set
│   ├── annotations
│   │   ├── label_map.pbtxt
│   │   ├── test_labels.csv
│   │   ├── train_labels.csv
│   │   ├── val_labels.csv        
|   ├── classes.txt
│   └── images

```

# Description

This dataset was used for Milestone 1 where the collages of images were created with objects overlapping each other.

You can create the TF records using the csv files using this python file in cs230-waste-classification-and-detection/data_processing :

```
For Training TF record :
python generate_tfrecord.py --csv_input=annotations/train_labels.csv --output_path=annotations/train.record --img_path=/images/train_set/ --label_map annotations/label_map.pbtxt

For Validation TF record :
python generate_tfrecord.py --csv_input=annotations/val_labels.csv --output_path=annotations/val.record --img_path=/images/val_set/ --label_map annotations/label_map.pbtxt
