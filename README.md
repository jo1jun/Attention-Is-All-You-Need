# Transformer 
## Paper : Attention Is All You Need / pdf : https://arxiv.org/pdf/1706.03762

## Transformer
nn.TransformerEncoder, nn.TransformerDecoder 을 이용하지 않고 custom 으로 직접 구현하였다.

## Transformer_module
nn.TransformerEncoder, nn.TransformerDecoderLayer 등의 이미 구현된 module 들을 이용하여 구현하였다.

refernce : https://pytorch.org/docs/master/generated/torch.nn.Transformer.html?highlight=transformer#torch.nn.Transformer

## dataset
기존에 학습했던 deep learning from scratch 2 에서 사용했던 dataset 을 이용하였다.

reference : https://github.com/jo1jun/deep-learning-from-scratch2/tree/main/dataset

## Coment
학습용으로 Deep Learning from scratch2 에서 다루어본 간단한 날짜 형식 dataset 으로 transformer 을 구현해 보았다.

핵심 이해 및 구현이 목적이므로 디테일은 추후에 다시 다루어볼 것.

TODO : code 내 TODO / another big dataset 에 적용해보기 / hyperparmeter tuning 
