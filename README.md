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
![image](https://user-images.githubusercontent.com/68524289/117619608-71fe9b00-b1aa-11eb-8142-be6417b52dca.png)
![image](https://user-images.githubusercontent.com/68524289/117619623-76c34f00-b1aa-11eb-9e80-a01e37177e86.png)
![image](https://user-images.githubusercontent.com/68524289/117619633-7a56d600-b1aa-11eb-9fda-d9c2041e5cb3.png)
![image](https://user-images.githubusercontent.com/68524289/117619645-7dea5d00-b1aa-11eb-81a8-2ad8fd78744f.png)
![image](https://user-images.githubusercontent.com/68524289/117619653-804cb700-b1aa-11eb-8fc3-8ebe8e13454d.png)
![image](https://user-images.githubusercontent.com/68524289/117619667-8347a780-b1aa-11eb-9a6d-87ca86641921.png)
![image](https://user-images.githubusercontent.com/68524289/117619675-85aa0180-b1aa-11eb-82ca-3325b1d4f44a.png)
![image](https://user-images.githubusercontent.com/68524289/117619683-88a4f200-b1aa-11eb-8f72-8279c9cae44e.png)
![image](https://user-images.githubusercontent.com/68524289/117619690-8b074c00-b1aa-11eb-8ef9-0dd70f401998.png)
![image](https://user-images.githubusercontent.com/68524289/117619702-8e023c80-b1aa-11eb-9726-ea6771ea1328.png)


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
