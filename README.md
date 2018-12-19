# Word2Vec
CBOW, SkipGram 모델을 사용해 기존 Neural Net Language Model (NNLM) 보다 성능을 높이면서 비용을 줄임

CBOW : k번째 단어의 앞뒤 n개씩의 단어(k-n, ..., k-1, k+1, ..., k+n)를 input으로 하여 k번째 단어를 output으로 한다.

SkipGram : k번째 단어를 input으로 하여 k번째 단어의 앞뒤 n개씩의 단어(k-n, ..., k-1, k+1, ..., k+n)를 output으로 한다.

Projection Layer없이, one-hot vector의 input에서 hidden layer를 거쳐 output 생성.

이 때, hidden layer로 보내는 matrix C를 학습하는데, C가 전체 V개의 단어에 대한 embedding 결과가 된다.



# Item2Vec
product recommendation with Item2Vec

- S3에 있는 View Log와 Order Log Data 활용
- Word2Vec 방식으로 각 Item을 Vector Space에 Embedding
- Item들간 Similarity 계산하여 연관 상품 추천


# Follow-Up Work
- Embeded item vector를 활용해 LSTM 적용 : 시계열 추천 > 개인화 추천 적용 가능
- Item Category, Item Name, Item Image 등의 Meta Data 추가 활용하여 Embedding
- User2Vec을 활용하여 User Clustering
