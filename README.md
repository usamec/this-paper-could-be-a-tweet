# This paper could be a tweet

This is a list of (mostly ML) papers where the description of the method contains a lot of fluff,
equation theatre, and it could be shortened significantly and explained much better.

This does not mean that the idea in the paper is bad or that the results of the mentioned papers are worthless. 
It just means that, in my opinion, they could be presented in a much better fashion.

## [LISA: Layerwise Importance Sampling for Memory-Efficient Large Language Model Fine-Tuning](https://arxiv.org/abs/2403.17919)

There is no importance sampling! Nothing. Zilch! The proposed optimizer always updates embedding and lm-head and randomly selects transformer blocks.
And they call this importance sampling, because the first and the last layer have a higher importance?
At least the results look promising. 

![image](https://github.com/user-attachments/assets/54a84e1a-7fd3-4bad-bb40-e613b7481120)


## [GhostNet: More Features from Cheap Operations](https://openaccess.thecvf.com/content_CVPR_2020/papers/Han_GhostNet_More_Features_From_Cheap_Operations_CVPR_2020_paper.pdf)

The idea is to replace (Pytorch pseudocode follow):
```
Conv2d(in, out, kernel_size)
```

With:
```
Sequential(
  Conv2d(in, small, kernel_size),
  Conv2d(small, out, kernel_size2, groups=small)
)
```

Aka factorized convolution in yet another way using smaller convolution + depthwise convolution.

## [Monarch: Expressive Structured Matrices for Efficient and Accurate Training](https://proceedings.mlr.press/v162/dao22a.html)

Instead of a bad figure and an important piece of algorithm hidden in the middle of the page:

![image](https://user-images.githubusercontent.com/1625559/204092542-bfbca618-86d0-4e2e-8644-470995f7ae52.png)

We could have a much better figure (parts taken from [Shufflenet](https://openaccess.thecvf.com/content_cvpr_2018/papers/Zhang_ShuffleNet_An_Extremely_CVPR_2018_paper.pdf)):

![image](https://user-images.githubusercontent.com/1625559/204092670-416ac394-2dae-4550-9fa5-6c99745c37e4.png)

With this, the paper could be understood in seconds instead of hours.

## [Locally Typical Sampling](https://arxiv.org/pdf/2202.00666)

30 pages of proofs, lingo, etc, could be simplified as:

![image](https://github.com/user-attachments/assets/053079b2-9b63-4582-8627-c50b0c7a20bc)

I.e., sample words whose log probability is close to entropy.

