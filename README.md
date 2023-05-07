Download Link: https://assignmentchef.com/product/solved-lab-10-neural-networks-and-deep-learning-data442-642
<br>
<strong>Exercise 1</strong>

This exercise focuses on the original GAN, which is trained on the MNIST database to learn to generate artificial hand-written characters. To implement and train the network, use the TensorFlow framework. You are encouraged to use the Keras high-level API for simplicity.

<ul>

 <li>Load the data set of 60000 to be used for training. Normalize image values so that allvalues are in the [−1<em>,</em>1] interval. In Keras, you may use the functions provided by the tensorflow.keras.datasets.mnist module.</li>

 <li>The generator is fed to its input with a noise vector and outputs an image. The dimensionof the input noise vector is 100, and its elements are i.i.d. sampled from a normal distribution of zero mean and unit variance. The generator consists of three fully connected layers with 256, 512, and 1024 neurons, respectively. The activation function used for the neurons in the hidden layers is the leaky ReLU with parameter <em>α </em>= 0<em>.</em> The output layer comprises 784 nodes and the tanh is employed as the respective activation function.</li>

 <li>The discriminator takes as input a 1 × 784 vector, corresponding to the vectorized form of the 28 × 28 MNIST images. The discriminator consists of three fully connected layers with 1024, 512, and 256 neurons, respectively. The leaky ReLU activation function is also employed, with <em>α </em>= 0<em>.</em> During training, use the dropout regularization method, with probability of discarding nodes equal to 0.3. The output layer consist of a single node with a sigmoid activation function.</li>

 <li>To train the implemented network, use the two-class (binary) cross-entropy loss function.Adopt the Adam minimizer with step size (learning rate) equal to 2×10<sup>−3</sup>, <em>β</em><sub>1 </sub>= 0<em>.</em>5, and <em>β</em><sub>2 </sub>= 0<em>.</em>999 as parameters for the optimizer. The recommended batch size is 100. Train the network for 400 epochs as follows. For each training loop, (a) generate a random set of input noise and images, (b) generate fake images via the generator, (c) train only the discriminator, and (d) then train only the generator, according to Algorithm 18.5. Play with the number of iterations, associated with the discriminator training.</li>

 <li>During training and every 20 epochs, visualize the generated images created by the generator and comment on the evolution of the learning process.</li>

 <li>Play with all the various parameters that have been suggested above and see the effect onthe training.</li>

</ul>