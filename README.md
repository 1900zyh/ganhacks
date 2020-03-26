# How to Train a GAN? Tips and tricks to make GANs work

Following suggestions come from [this post](https://medium.com/@utk.is.here/keep-calm-and-train-a-gan-pitfalls-and-tips-on-training-generative-adversarial-networks-edd529764aa9)

## 1: Larger kernels and more filters
- Larger kernels in G at the top convs can maintain some kind of smoothness. 
- Using less filters in G make the final generated images too blurry. 

## 2: Soft and Noisy labels 
- For training discriminators, fake label: 0~0.1, real label: 0.9~1.0
- Randomly flip labels to penalize initial gradients. 

## 3: Look at the Gradients 
- Monitor the gradients along with the losses in the networks. 
- G should receive large gradients early, while D's is not large. Later, the gradient of D should get stronger. 

Following suggestions come from [this post](https://medium.com/intel-student-ambassadors/tips-on-training-your-gans-faster-and-achieve-better-results-9200354acaa5)

## 4: Upsampling vs Transposed Convolution 
- Use upsampling instead of transposed convolution 
- The kernel size of convolutions would better to be divided by stride 

## 5: Loss functions 
- WGAN is better than NSGAN. 
- Have a try on RaLS. 




