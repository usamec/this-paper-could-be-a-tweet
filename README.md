# This paper could be a tweet

This is a list of (mostly ML) papers, where description of the method contains a lot of fluff,
equation theatre and it could be shortened significantly and explained much better.

This does not mean that idea in paper is bad or results of mentioned papers are worthless. 
It just means, that in my opinion, they could be presented in much better fashion.

## [GhostNet: More Features from Cheap Operations](https://openaccess.thecvf.com/content_CVPR_2020/papers/Han_GhostNet_More_Features_From_Cheap_Operations_CVPR_2020_paper.pdf)

Idea is to replace (Pytorch pseudocode follow):
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

Instead of a bad figure and important piece of algorithm hidden in the middle of the page:

![image](https://user-images.githubusercontent.com/1625559/204092542-bfbca618-86d0-4e2e-8644-470995f7ae52.png)

We could have much better figure (parts taken from [Shufflenet](https://openaccess.thecvf.com/content_cvpr_2018/papers/Zhang_ShuffleNet_An_Extremely_CVPR_2018_paper.pdf)):

![image](https://user-images.githubusercontent.com/1625559/204092670-416ac394-2dae-4550-9fa5-6c99745c37e4.png)

With this, paper could be understood in seconds instead of hours.


