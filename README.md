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
## [Principal Component Analysis](http://www.nlpca.org/pca_principal_component_analysis.html)
![](http://www.nlpca.org/fig_pca_principal_component_analysis.png)
Principal Component Analysis, or PCA, is a dimensionality-reduction method that is often used to reduce the dimensionality of large data sets, by transforming a large set of variables into a smaller one that still contains most of the information in the large set.
- PCA provides a normalisation that accounts for correlations between
features.
- PCA finds a change of basis for the data.
- The first principal component is the direction in which the variance is
highest.
### second Principal Component orthogonal to the first one
![](https://cdn-images-1.medium.com/max/1600/1*3rDxjskx9V_aEuKeLYX5cw.png)


- [Everything you did and didn't know about PCA](http://alexhwilliams.info/itsneuronalblog/2016/03/27/pca/)
- [article: step-by-step-explanation-of-principal-component-analysis](https://towardsdatascience.com/a-step-by-step-explanation-of-principal-component-analysis-b836fb9c97e2)
- [video: Principal Component Analysis (PCA)](https://www.youtube.com/watch?v=g-Hb26agBFg)

## [Eigenfaces](http://lpsa.swarthmore.edu/MtrxVibe/EigMat/MatrixEigen.html)



# [5 Probability 1: Entropy, (Naive) Bayes, Cross-entropy loss (MLVU2019)](https://www.youtube.com/watch?v=IMwiu64wgCU)
## [Entropy](https://rdipietro.github.io/friendly-intro-to-cross-entropy-loss/#entropy)
- [A Short Introduction to Entropy, Cross-Entropy and KL-Divergence](https://www.youtube.com/watch?v=ErfnhcEV1O8)


# [6 Linear Models 2: Neural Networks, Backpropagation, SVMs and Kernel methods](https://www.youtube.com/watch?v=g2lziWxf_9Q)
## [backpropagation](https://www.google.com/url?sa=t&rct=j&q=&esrc=s&source=web&cd=3&cad=rja&uact=8&ved=2ahUKEwjK4-vXoJjhAhVMJ1AKHbCJDU0QwqsBMAJ6BAgJEAc&url=https%3A%2F%2Fwww.youtube.com%2Fwatch%3Fv%3DFaHHWdsIYQg&usg=AOvVaw0cLk7Tqe50zqUnDEcbYnVl)
- another name for gradiant discent
- Backpropagation is about understanding how changing the weights and biases in a network changes the cost function. 
- The goal of backpropagation is to compute the partial derivatives ∂C/∂w and ∂C/∂b of the cost function C with respect to any weight w or bias b in the network.
- Backpropagation is based around four fundamental equations. Together, those equations give us a way of computing both the error δl and the gradient of the cost function. 

![http://neuralnetworksanddeeplearning.com/chap2.html](http://neuralnetworksanddeeplearning.com/images/tikz21.png)
- [source](http://neuralnetworksanddeeplearning.com/chap2.html)

## [SVM Soft-margin vs Hard margin](http://people.csail.mit.edu/dsontag/courses/ml14/slides/lecture2.pdf)
![](https://qph.fs.quoracdn.net/main-qimg-0a3e8d1f008e7e86c10efe9936ead943)
- hard margin works only with fully linear peparable data 
- soft margin extends hard margin allowing erorrs to be made fitting the model
### Kernel svm
![](http://www.eric-kim.net/eric-kim-net/posts/1/imgs/data_2d_to_3d.png)
- introduce another axe-z and find a function that allow us to extract common z-axe value for  each group of points.
    - Pros: Provides a principled way of solving the multiclass problem.
    - Cons: Multiclass extensions tend to be much more complicated than the original binary 
***

# [9 Deep Learning 2: GANs and VAEs (MLVU2019)](https://www.youtube.com/watch?v=6N4zIx0ATME)
## generative adversarial networks
The original GAN was created by Ian Goodfellow, who described the GAN architecture in a [paper published in mid-2014](https://papers.nips.cc/paper/5423-generative-adversarial-nets.pdf).
The discriminator tries to determine whether information is real or fake. The other neural network, called a generator, tries to create data that the discriminator thinks is real. We have a generator network and discriminator network playing against each other. The generator tries to produce samples from the desired distribution and the discriminator tries to predict if the sample is from the actual distribution or produced by the generator. The generator and discriminator are trained jointly. The effect this has is that eventually the generator learns to approximate the underlying distribution completely and the discriminator is left guessing randomly.
## Vanilla GAN
The original GAN is called a vanilla GAN.
![](https://cdn-images-1.medium.com/max/1600/1*--AtNcFUNb_ts_uihuSJ2g.png)
![](https://s3-ap-south-1.amazonaws.com/av-blog-media/wp-content/uploads/2017/06/11000153/g1.jpg)
## Conditional GAN
![](https://i.stack.imgur.com/nnAkj.gif)
## CycleGANs
![](https://hardikbansal.github.io/CycleGANBlog/images/model1.jpg)
## Style GAN
![](https://www.lyrn.ai/wp-content/uploads/2018/12/StyleGAN-generator-AdaIN.png)
 ## Autoencoders
 Autoencoders encode input data as vectors. They create a hidden, or compressed, representation of the raw data. They are useful in dimensionality reduction; that is, the vector serving as a hidden representation compresses the raw data into a smaller number of salient dimensions. Autoencoders can be paired with a so-called decoder, which allows you to reconstruct input data based on its hidden representation, much as you would with a restricted Boltzmann machine.
 - useful for image trasmission low-bandwith
 ![](https://skymind.ai/images/wiki/autoencoder_schema.jpg)

### Other videos:
- [video: Generative Adversarial Networks (GANs) - How and Why They Work](https://youtu.be/ZRgwcMqxhPw)
- [video: Turning Fortnite into PUBG with Deep Learning (CycleGANs)](https://youtu.be/xkLtgwWxrec)




***

## Generative VS Discriminative Models
- [article: “is this animal a lion or an elephant?”](https://medium.com/@mlengineer/generative-and-discriminative-models-af5637a66a3)
