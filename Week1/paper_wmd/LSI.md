https://blog.csdn.net/qq_37098526/article/details/89394880


原来的SVD， 降rank
用之前的得到的代表每一zhi每一zhi

$$
A= USV^T
$$
query: q = 11 * 1

A = 11 * 3 (11 word x 3 docs)
U = 11 * 3  -> U_k = 11 * 2 (11 word, 2 feature)
S = 3 * 3   -> S_k = 2 * 2  (strength of each feature)
V = 3 * 3   -> V_k = 3 * 2  (3 docs, 2 feature)

所以decompose之后得到的就是V_k里面的一个row代表一个doc的vector

U， S 相当于根据A 训练得到的结果

这时候我们把q，根据我们的训练结果U，S "train"一个feature vector

U, V are orthonormal, have $U^T = U^{-1}$

$$
q' = q^T U_k S_K^{-1}
$$
推导可得到by $q = U_k S_k q'^T$

之后再用cosine similarity 可以得到
 