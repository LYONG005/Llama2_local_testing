# Testing Llama2

This repository explains 2 different methods of how we can 
test Llama2 on the <b>cloud</b> using Google Collab or <b>locally</b> via huggingface.
<br>

## Cloud Testing
To test Llama2 on the cloud via Google collab we can head over to 
Camenduru's Repository: https://github.com/camenduru/text-generation-webui-colab <br>

Under the README.md choose the model in which you like to test and 
run the google collab accordingly.

## Local Testing
To test Llama2 locally via huggingface we will follow Martin Thissen's Medium article found
here: https://medium.com/p/41b7638033a8 (requires login and premium membership)

Clone the repository and install the requirements using these commands:

```git clone https://github.com/thisserand/llama2_local.git``` <br>
```cd llama2_local``` <br>
```pip install -r requirements.txt```<br>

Next we would need to log into our Hugging Face account to download the model weights and tokenizer using this command:
<br>
``huggingface-cli login``

You will be asked for your Huggingface access token, which you can find here https://huggingface.co/settings/tokens <br>

### Full Precision (Original)
Llama2-7B:
```python llama.py --model_name="meta-llama/Llama-2-7b-hf"```

Llama2-7B-Chat:
```python llama.py --model_name="meta-llama/Llama-2-7b-chat-hf"```

Llama2-13B:
```python llama.py --model_name="meta-llama/Llama-2-13b-hf"```

Llama2-13B-Chat:
```python llama.py --model_name="meta-llama/Llama-2-13b-chat-hf"```

Llama2-70B:
```python llama.py --model_name="meta-llama/Llama-2-70b-hf"```

Llama2-70B-Chat:
```python llama.py --model_name="meta-llama/Llama-2-70b-chat-hf"```

### GPTQ Quantized
Llama2-7B:
```python llama.py --model_name="TheBloke/Llama-2-7B-GPTQ"```

Llama2-7B-Chat:
```python llama.py --model_name="TheBloke/Llama-2-7b-Chat-GPTQ"```

Llama2-13B:
```python llama.py --model_name="TheBloke/Llama-2-13B-GPTQ"```

Llama2-13B-Chat:
```python llama.py --model_name="TheBloke/Llama-2-13B-Chat-GPTQ"```

Llama2-70B:
```python llama.py --model_name="TheBloke/Llama-2-70B-GPTQ"```

Llama2-70B-Chat:
```python llama.py --model_name="TheBloke/Llama-2-70B-Chat-GPTQ"```

### CGML Quantized
Llama2-7B:
```python llama.py --model_name="TheBloke/Llama-2-7B-GGML" --file_name="llama-2-7b.ggmlv3.q4_K_M.bin"```

Llama2-7B-Chat:
```python llama.py --model_name="TheBloke/Llama-2-7B-Chat-GGML" --file_name="llama-2-7b-chat.ggmlv3.q4_K_M.bin"```

Llama2-13B:
```python llama.py --model_name="TheBloke/Llama-2-13B-GGML" --file_name="llama-2-13b.ggmlv3.q4_K_M.bin"```

Llama2-13B-Chat:
```python llama.py --model_name="TheBloke/Llama-2-13B-Chat-GGML" --file_name="llama-2-13b-chat.ggmlv3.q4_K_M.bin"```

