## Overview
This repo consists of PEFT methods for comparison of multi-lingual pretrained language models

## How to run the code

For XNLI comparison


```
python run_xnli.py --model_name_or_path bert-base-multilingual-cased --language es --train_language en --do_train --do_eval --per_device_train_batch_size 256 --num_train_epochs 3 --max_seq_length 128 --output_dir /temp --overwrite_output_dir --peft_choice lora
```

For PAWS-X comparison

```
python run_glue.py --model_name_or_path bigscience/bloom-560m --dataset_name paws-x --dataset_config de --per_device_train_batch_size 256 --num_train_epochs 1 --max_seq_length 128 --output_dir /temp --overwrite_output_dir --peft_choice lora --do_train --do_eval
```