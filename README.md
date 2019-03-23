# Machine Learning Notes
## What is machine learning?
![](https://railsware.com/blog/wp-content/uploads/2018/09/illustration-2b-1024x728.jpg)

# [2 Linear Models 1: Hyperplanes, Random Search, Gradient Descent (MLVU2019)](https://youtu.be/3K4pNmQbGx8?t=2550)
## Hyperplanes
- dot product 
- 2d linear function
## Random Search
- optimization random search:
it test if the next random point is better than the previous one and if yes it switch, from probability q now and then we test if there is another better solution and check if there is a global minimum or we already reach it. 
  - if loss(p) < loss(p')
    - p <- p'
  - else:
    - probability q: p <- p'
- compute only loss function 
- require many interaction
- work with trees discrete models
- can be parallelized 
## Gradient descent
![](https://cdn-images-1.medium.com/max/1600/1*f9a162GhpMbiTVTAua_lLQ.png)
### Definitions
Gradient Descent requires a cost function(there are many types of cost functions). We need this cost function because we want to minimize it. Minimizing any function means finding the deepest valley in that function. Keep in mind that, the cost function is used to monitor the error in predictions of an ML model. So minimizing this, basically means getting to the lowest error value possible or increasing the accuracy of the model. In short, We increase the accuracy by iterating over a training data set while tweaking the parameters(the weights and biases) of our model.
#### So, the whole point of GD is to minimize the cost function.
- Gradient descent computes the direction of steepest descent.
- Accuracy is a bad loss function in gradient descent, becasue gradient descent makes the gradient zero almost everywhere.
- no escape local minima

***

# [4 Methodology 2: Data cleaning, Principal Component Analysis, Eigenfaces (MLVU2019)](https://www.youtube.com/watch?v=H4c4qpHdGq8)
## Principal Component Analysis
![](http://www.nlpca.org/fig_pca_principal_component_analysis.png)
### Definitions
Principal Component Analysis, or PCA, is a dimensionality-reduction method that is often used to reduce the dimensionality of large data sets, by transforming a large set of variables into a smaller one that still contains most of the information in the large set.
- PCA provides a normalisation that accounts for correlations between
features.
- PCA finds a change of basis for the data.
- The first principal component is the direction in which the variance is
highest.

- [Everything you did and didn't know about PCA](http://alexhwilliams.info/itsneuronalblog/2016/03/27/pca/)
- [article: step-by-step-explanation-of-principal-component-analysis](https://towardsdatascience.com/a-step-by-step-explanation-of-principal-component-analysis-b836fb9c97e2)
- [video: Principal Component Analysis (PCA)](https://www.youtube.com/watch?v=g-Hb26agBFg)

## Eigenfaces



# [5 Probability 1: Entropy, (Naive) Bayes, Cross-entropy loss (MLVU2019)
](https://www.youtube.com/watch?v=IMwiu64wgCU)
## Entropy 
- [A Short Introduction to Entropy, Cross-Entropy and KL-Divergence](https://www.youtube.com/watch?v=ErfnhcEV1O8)




## CycleGANs
## Definitions
### VU material Week 10: 
- [VU video1](https://www.youtube.com/watch?v=6N4zIx0ATME&feature=youtu.be)

### Other videos:
- [video: Generative Adversarial Networks (GANs) - How and Why They Work](https://youtu.be/ZRgwcMqxhPw)
- [video: Turning Fortnite into PUBG with Deep Learning (CycleGANs)](https://youtu.be/xkLtgwWxrec)

***

## Generative VS Discriminative Models
- [article: “is this animal a lion or an elephant?”](https://medium.com/@mlengineer/generative-and-discriminative-models-af5637a66a3)
