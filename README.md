# Generative-Adversarial-Networks-GAN-
GAN architecture is a genius setup that has unlocked the potential for realistic data generation and augmentation.

Generative Adversarial Networks are deep learning machines that combine two separate models into one architecture. The two components are:

•	Generator Model

•	Discriminator Model

•	The two models compete against each other in a zero-sum game. The generator model tries to generate new data samples similar to those in the problem domain. Meanwhile, the discriminator tries to identify whether the example presented is fake (comes from a generator ) or real (comes from the actual data domain).

•	The competition between the generator and the discriminator makes them adversaries, which gives the name to GANs.

Steps of the algorithm: 

Generator Model part: 

1.	The generator model samples a random vector from the latent space. This space follows Gaussian distribution with the number of dimensions specified by us. The random vector seeds the generative process since we use it as input to our neural network.
  
2.	The inputs follow a standard path through the network with one or multiple hidden layers. In the case of a simple GAN, this would be a bunch of densely connected layers, while Deep Convolutional GAN (DCGAN) would also incorporate convolutional layers.
  
3.	The data flows into an output layer where we can make final adjustments to ensure that the generator output has the required shape to feed into a discriminator.
  
4.	Finally, we can use these fake (generated) samples to try and fool the discriminator.

Discriminator model part: 

1.	The inputs to the discriminator model are a combination of real samples (drawn from the problem domain) and fake ones (created by the generator model).
  
2.	The data goes through the network with one or multiple hidden layers, the same as what you would have in any other neural network.
	
3.	Once we reach the output layer, the discriminator decides whether the sample is real or fake (generated).
   
The discriminator is no different from a standard neural network classification model.

To summarize: We want to train the generator G such that it will produce the results for the discriminator D so that D won’t be able to distinguish between z, vector inputs from the Generator, and X. Creating Fake images by the Generator Model as similar as the real ones. So the optimal state of D will be P(x)=0.5. 

