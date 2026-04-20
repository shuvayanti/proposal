This repository contains the code to an experiment to visualise hindi character representation in the inner layers of a finetuned Llama-2 model on hindi language. Teh experiment was conducted on colab with limited resources.

Procedure:

1. *Data Creation & tokenizers* - The methods mentioned in the [Llama-cookbook multilingual](https://github.com/meta-llama/llama-cookbook/tree/main/end-to-end-use-cases/multilingual) recipie has been used. 1043 Hindi paragraphs were selected from the [Varta](https://huggingface.co/datasets/rahular/varta) dataset for the training purpose. The data is stored [here](https://huggingface.co/datasets/shuvayanti/data)
2. *Finetune* the model. Evaluate. The [finetuned](https://huggingface.co/shuvayanti/finetuned-hindi-llama-model) and [merged](https://huggingface.co/shuvayanti/merged-finetuned-hindi-llama-model) model have been uploaded to huggingface. The model was trained for only 1 epoch. With more epochs the loss and perplexity does reduce significantly but the weight of the resulting model also increases due to addition checkpoints which is difficult to store with limited disk space.
3. *Train tuned lens* on the new model and the dataset([Trained lens](https://huggingface.co/shuvayanti/trained-tuned-lens)).
4. *Plot*.

Results:

*Tuned Lens* - The plot shows that character representation in a finetuned model maintains its linguistic properties. The plot lacks clarity because of training with limited data. With more data and additiion training maybe we will achieve beter representation.

*Logit lens* - the plot contains undefined characters in the inner layers becuase the les wasn't trained on the data and the finetuned model. The base model ([meta-llama/Llama-2-7b-chat-hf](https://huggingface.co/meta-llama/Llama-2-7b-chat-hf)) was used to create the lens which unfortunately couldn't identify hindi characters.
