This repository contains the code to an experiment to visualise hindi character representation in the inner layers of a finetuned Llama-2 model on hindi language. 

Procedure:
1. Data Creation & tokenizers - The methods mentioned in the [Llama-cookbook multilingual](https://github.com/meta-llama/llama-cookbook/tree/main/end-to-end-use-cases/multilingual) recipie has been used. 1043 Hindi paragraphs were selected from the [Varta](https://huggingface.co/datasets/rahular/varta) dataset for the training purpose. The data is stored [here](https://huggingface.co/datasets/shuvayanti/data)
2. Finetune the model. Evaluate. The [finetuned](https://huggingface.co/shuvayanti/finetuned-hindi-llama-model) and [merged](https://huggingface.co/shuvayanti/merged-finetuned-hindi-llama-model) model have been uploaded to huggingface.
3. Train tuned lens on the new model and the dataset([Trained lens](https://huggingface.co/shuvayanti/trained-tuned-lens)).
4. Plot.

Results:
