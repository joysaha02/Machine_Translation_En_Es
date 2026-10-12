# Machine Translation: English → Spanish

A Transformer model built from scratch in PyTorch, based on [*Attention Is All You Need*](https://arxiv.org/abs/1706.03762), and trained to translate English into Spanish.

## Results

| English | Model output |
|---|---|
| Where is my brother? | ¿Dónde está mi hermano? |
| The night was dark and cold. | La noche estaba muy oscura y fría. |
| I do not know what you mean, sir. | No sé qué piensa, señor. |
| Wait a moment, I'll give him to you. | Espera, os lo daré un momento. |

## Training

| | |
|---|---|
| Dataset | [OPUS Books](https://huggingface.co/datasets/Helsinki-NLP/opus_books) (en-es), 93,470 sentence pairs |
| Model | 6 encoder + 6 decoder layers, 8 heads, d_model 512 (~90M parameters) |
| Epochs | 20 |
| GPU | NVIDIA RTX 5090 |
| Training time | ~2.5 hours |
| Final loss | 2.50 |

## Usage

```bash
pip install -r requirements.txt
python train.py
python translate.py "Where is my brother?"
```

## Files

| File | Description |
|---|---|
| `model.py` | Transformer architecture |
| `dataset.py` | Data preprocessing |
| `config.py` | Settings |
| `train.py` | Training |
| `translate.py` | Translation |
| `notebooks/` | Inference, beam search, attention visualization |
