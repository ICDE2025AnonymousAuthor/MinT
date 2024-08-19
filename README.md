# MinT

This is the implementation for our AAAI2025 paper:
> Medical Match, Personal Touch: A Dual-Module Approach for Tailored Doctor Recommendations

## Environment
We use Python language and Pytorch library to establish our model. 

For the detailed environment, please follow `requirements.txt`

## Dataset
We crawl the data from the Haodf website, the dataset is released at [Haodf.zip](./Haodf.zip)

## Run *MinT*
### Data Preprocess
First, unzip the dataset with
```
unzip Haodf.zip -d ./Dataset
```
Then generate datasets through
```
python ./Script/dataset_process.py
```
### Train and Evaluate *MinT* 
Run *MinT* with 
```
python ./MinT/main.py --dataset=diab --batch_size=16 --lr_recall=0.01 --lr_rank=0.001 --embed_size=64
```
For different dataset, select `--dataset={dataset}` from `dataset={'diab', 'cold', 'CHD', 'lung', 'depr', 'pneu'}`
