# Action-Recognition

##Action Recognition on KTH Dataset.

1. We used the STIP Binaries found at [here] (https://www.di.ens.fr/~laptev/download.html#stip) , to extract the STIPs with the HOG-HOF descriptors.
2. The descriptors extracted are then clustered -using k-means with 3000 cluster- in order to form a visual codebook with 3000 words.
![Bag Of Words](/images/pipeline.png)
3. A Bag of words is then constructed for each example (video sequence)  based on the occurrences of the codewords in the given example.
4. The examples (3001-vector-BoW+Label) are then classified using Multi-Class non-Linear SVM.
