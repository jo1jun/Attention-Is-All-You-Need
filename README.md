# Transformer 
## Paper : Attention Is All You Need / pdf : https://arxiv.org/pdf/1706.03762

## Transformer.ipynb
nn.TransformerEncoder, nn.TransformerDecoder 을 이용하지 않고 custom 으로 직접 구현하였다.

## Transformer_module.ipynb
nn.TransformerEncoder, nn.TransformerDecoderLayer 등의 이미 구현된 module 들을 이용하여 구현하였다.

refernce : https://pytorch.org/docs/master/generated/torch.nn.Transformer.html?highlight=transformer#torch.nn.Transformer

## dataset
date.txt    : 날짜 형식 data set
sequence.py : data load / id-to-char / char-to-id 등의 util
기존에 학습했던 deep learning from scratch 2 에서 사용했던 dataset 을 이용하였다.

reference : https://github.com/jo1jun/deep-learning-from-scratch2/tree/main/dataset

original  : https://github.com/WegraLee/deep-learning-from-scratch-2/tree/master/dataset

## result
### attention example
![image](https://user-images.githubusercontent.com/68524289/117152229-cbef1180-adf4-11eb-9980-83b60b3edfc5.png)
![image](https://user-images.githubusercontent.com/68524289/117152144-b4b02400-adf4-11eb-85e3-62f2d6f19924.png)
![image](https://user-images.githubusercontent.com/68524289/117153461-f2fa1300-adf5-11eb-9c97-20c8f17c44f1.png)
![image](https://user-images.githubusercontent.com/68524289/117153505-01482f00-adf6-11eb-8432-93ba7bcb8252.png)

### generation example
question 1 :  1 0 / 1 5 / 9 4                                          
correct 1  :  1 9 9 4 - 1 0 - 1 5                                          
predict 1  :  1 9 9 4 - 1 0 - 1 5

question 2 :  t h u r s d a y ,   n o v e m b e r   1 3 ,   2 0 0 8    
correct 2  :  2 0 0 8 - 1 1 - 1 3                                           
predict 2  :  2 0 0 8 - 1 1 - 1 3

question 3 :  M a r   2 5 ,   2 0 0 3                                  
correct 3  :  2 0 0 3 - 0 3 - 2 5                                           
predict 3  :  2 0 0 3 - 0 3 - 2 5

question 4 :  T u e s d a y ,   N o v e m b e r   2 2 ,   2 0 1 6      
correct 4  :  2 0 1 6 - 1 1 - 2 2                                           
predict 4  :  2 0 1 6 - 1 1 - 2 2

question 5 :  S a t u r d a y ,   J u l y   1 8 ,   1 9 7 0            
correct 5  :  1 9 7 0 - 0 7 - 1 8                                           
predict 5  :  1 9 7 0 - 0 7 - 1 8

question 6 :  o c t o b e r   6 ,   1 9 9 2                            
correct 6  :  1 9 9 2 - 1 0 - 0 6                                           
predict 6  :  1 9 9 2 - 1 0 - 0 6

question 7 :  8 / 2 3 / 0 8                                            
correct 7  :  2 0 0 8 - 0 8 - 2 3                                           
predict 7  :  2 0 0 8 - 0 8 - 2 3

question 8 :  8 / 3 0 / 0 7                                            
correct 8  :  2 0 0 7 - 0 8 - 3 0                                           
predict 8  :  2 0 0 7 - 0 8 - 3 0

question 9 :  1 0 / 2 8 / 1 3                                          
correct 9  :  2 0 1 3 - 1 0 - 2 8                                           
predict 9  :  2 0 1 3 - 1 0 - 2 8

question 10 :  s u n d a y ,   n o v e m b e r   6 ,   2 0 1 6          
correct 10  :  2 0 1 6 - 1 1 - 0 6                                            
predict 10  :  2 0 1 6 - 1 1 - 0 6

## Comment
학습용으로 Deep Learning from scratch2 에서 다루어본 간단한 날짜 형식 dataset 으로 transformer 을 구현해 보았다.

핵심 이해 및 구현이 목적이므로 디테일은 추후에 다시 다루어볼 것.

TODO : code 내 TODO / two embedding layers and pre-softamx linear layer weight share / label smoothing / another big dataset 에 적용해보기 / 응용 task 에 접목
