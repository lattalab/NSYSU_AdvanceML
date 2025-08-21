## NSYSU_AdvanceML
NSYSU 2025 spring semester course  
CSE523 `進階機器學習 ADVANCED MACHINE LEARNING`  
Instructor: 張雲南 (Yun-Nan Chang)

* HW1  
  1. Design a simple MLP (Multilayer perceptron) to classify circles_data.
     After training, drawing a decision boundary plot
  2. Do a math calculation about `Gradient Descent`.
* HW2
  * Dataset: MNIST with some modification like digit at different position.  
  1. Train a CNN on custom MNIST dataset (different that the network searched version)
  2. Show the `accuary` and `confusion matrix` of top1 and top3
  3. calculate the value of $$\frac{top \ 1 \ accuracy}{number \ of \ weights}$$
  4. Use such trained model to try to predict the result on Testing data and store the result into a CSV file.
* HW3  
    * Dataset: HW2_MNIST、HW3_text.csv  
    
    Use RNN (including LSTM and GRU) model to do `classification`, `sentimental classification`, `NLP word prediction` tasks and show the accuracy statistics and confusion matrix.  
    More information are writed in README in the HW3 folder.
 * HW4  
    * Dataset: HW2_MNIST_train、HW3_text.csv
    1. using `CLIP` on HW2_MNIST_train, and show the top1、top3 evaluating result.
    2. using `BERT` to do text-classification on HW3_text.csv. Provided the test result with `confusion matrix` as well.
    3. Calculate the LLaMA2-7B weights.
    4. Question-Answering (QA) system with Chroma vector database.
    Here, also implemented the RAG(Retrival-Augmented Generation), but not necessary in this homework.
    5. Perform `Image-Text Matching` task with `BLIP`.
  
    If you don't want to download a large amount of model parameter, you can use `google colab` to run the file, as I do in HW4_4.ipynb and HW4_5.ipynb .
* HW5  
    * Dataset: MNIST、Fashion-MNIST  

  Learn `Anomaly Detection`, `Auto-encoder` and `GAN` from the question set.  
  * Key of Anomaly Detection: you need to determine threshold to justify `Normal` and `Abnormal` data.
  * By compared with `VAE` and `Auto-Encoder`, you may know more about `KL-divergence`.
  * Theoretically, the training stability can be ranked as `GAN < WGAN < WGAN-GP`.  
  However, I got the best result with `GAN`, it may due randomized-generated data.