# IIR新生訓練HW6
## Q1
- Order 0
    - transition matrix
    ```
    [0.31515 0.20803 0.20796 0.26886]
    ```
    - Probability
        - -197688.94757657658 (in log base 2)
- Order 1
    - transition matrix
    ```
    [[0.35529113 0.17569411 0.22862129 0.24039346]
     [0.37475364 0.25515551 0.050137   0.31995385]
     [0.30204376 0.21216639 0.25765809 0.22813176]
     [0.23212825 0.20627836 0.26742543 0.29416797]]
     ```
    - Probability
        - -193211.2529998648 (in log base 2)
- Order 2
    - transition matrix
    ```
    [[[0.41537912 0.15361257 0.19665982 0.23434849]
      [0.42297273 0.22846307 0.05111071 0.29745349]
      [0.33282443 0.20721721 0.24941013 0.21054823]
      [0.28220697 0.17014256 0.25527983 0.29237064]]
     [[0.27988712 0.21241662 0.27591072 0.23178553]
      [0.3637905  0.25395629 0.05256217 0.32969103]
      [0.24544583 0.2253116  0.28283797 0.2464046 ]
      [0.19215745 0.23527644 0.31805889 0.25450721]]
     [[0.34819296 0.16143926 0.27479701 0.21557077]
      [0.34088849 0.28286491 0.05847688 0.31776972]
      [0.30851064 0.22956327 0.25531915 0.20660694]
      [0.22533727 0.19709106 0.32630691 0.25126476]]
     [[0.3488223  0.18378465 0.1804198  0.28697324]
      [0.36404616 0.26090876 0.04020916 0.33483592]
      [0.27458617 0.20225344 0.26401447 0.25914592]
      [0.22192716 0.22205362 0.20106222 0.35495701]]]
  ```
    - Probability
        - -192098.42731591314 (in log base 2)
## Q2
- Compute the log base 2 probability of your model generating S
    - Probability: -193886.45502556668 log base on 2
- Compute the most likely state sequence that the model would traverse when emitting S.
![](https://i.imgur.com/PgqxEOR.png)
- Compute the probabilities that they would generate another 100kb section of the human genome.
![](https://i.imgur.com/nLJ2V0p.png)
## Report
- Running time & Memory usage

![](https://i.imgur.com/TkKRkQ5.png)

### 參考網站
- [hmmlearn Tutorial](https://hmmlearn.readthedocs.io/en/latest/tutorial.html#building-hmm-and-generating-samples)
- [Hidden Markov Model](https://medium.com/ai-academy-taiwan/hidden-markov-model-part-2-ac46dcdd42d1)
- [用hmmlearn学习隐马尔科夫模型HMM](https://www.cnblogs.com/pinard/p/7001397.html)
- [hmm.GaussianHMM参数解析](https://zhuanlan.zhihu.com/p/46303947)
