# Generative Adversarial Network (GAN)
>Artificial intelligence aims to enable machines to think like humans. Deep Learning is a subfield of machine learning that takes inspiration from the structure and the function of the brain. Deep learning has achieved great success in generating images. 

>Generative Adversarial Network (GAN) is an unsupervised learning type that involves automatically discovering and learning patterns in input data to generate new examples by appropriately extracting from the original dataset. Unlike classical deep neural network architectures, it has two distinct deep networks: a generator (G) and a discriminator (D). The Discriminator model is a convolutional classifier that classifies incoming images as real or fake. The Generator model is slightly more complex. This essentially involves a process called inverse convolution. It attempts to deceive the Discriminator classifier with the newly generated images. During training, the Generator gets better at creating realistically looking images while the Discriminator gets better at distinguishing them. The process reaches equilibrium when the Discriminator can no longer distinguish real images from fakes. It can be used in various fields such as creating new image datasets, generating high-resolution realistic photographs, creating cartoon characters, and translating text to images. GANs offer advantages such as promising powerful unsupervised learning and the possibility of generating high-quality synthetic data.

>MNIST dataset(Figure 1) was used in this project. Synthetic data were generated with GANs. During the project experiments, the loss functions ”Hinge Loss”,  "BCELoss" and "BCEWithLogitsLoss" (Figure 2) were tested, and it was found that "BCELoss" performed better in this problem. Different learning rate (LR) values were also tried, and the ideal LR for this project was determined as "0.0002" (Figure 3, Figure 4). The activation functions "ReLU" and "Sigmoid" were used in the discriminator, while "ReLU" and "Tanh" were used in the generator. When the "Sigmoid" activation function was used as the output function, poor results were obtained. The optimization parameters of Adam and SGD were tested, and Adam optimization performed better (Figure 5). The model was trained for 10 epochs, but it was found to be insufficient to learn the data. When simpler discriminator and generator models are used the loss values are higher than the current ones (Figure 6). The current output is shown in Figure 7, where BCELoss, Learning Rate = 0.0002, ReLU, Sigmoid and Tanh activation functions, and Adam optimization are used.
> Figure 1. MNIST Data

![image](https://user-images.githubusercontent.com/82284108/232318233-be29a51e-3743-4fb8-9ff4-bb8566e80141.png)


>Figure 2. After 10 epochs, the output was obtained using BCEWithLogitsLoss.

![image](https://user-images.githubusercontent.com/82284108/232318343-13ee850b-13aa-41c8-a025-d5c176f38c62.png)



>Figure 3. 10 epoch BCELoss, Adam optimizer and Learning Rate = 0.0001 

![image](https://user-images.githubusercontent.com/82284108/232318378-34741910-ef32-4e84-847d-8fa8ec03c645.png)


>Figure 4. 10 epoch BCELoss, Adam optimizer and Learning Rate = 0.0002

![image](https://user-images.githubusercontent.com/82284108/232318422-3c132b3b-0a50-4cb7-9f6e-9d47f884a7ff.png)

>Figure 5. The output obtained with SGD optimization after 10 epochs (Learnin Rate = 0.0001).

![image](https://user-images.githubusercontent.com/82284108/232318543-b69b0f23-371c-44f3-a7e1-77af58a0d4e8.png)


>Figure 6. Simpler discriminator and generator

![image](https://user-images.githubusercontent.com/82284108/232318574-78e703f9-117b-4709-8b0f-743b248635a9.png)


>Figure 7. BCELoss, Learning Rate = 0.0002, ReLU, Sigmoid and Tanh activation functions, and Adam optimizer

![image](https://user-images.githubusercontent.com/82284108/232318612-9491ef10-a088-4815-b37e-9a68deedffcb.png)

