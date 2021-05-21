# session3_pytoroch

group 25 members - 
1)Ashok(me)
2)Gokul

# data generation
i) data is taken from MNIST data set. It has 60,000 images. 59,000 images are considered for training and 1000 for validation
ii)DataLoader is used to create batch size of 100

#model
i)All the convolutional layers are of 3x3 kernel size. The no.of kernels are increased from 8 to 16 to 32 to 64 
ii)All the maxpool layers are of 2x2 size with stride 2
iii)self.out1 gives the size 10 output related to MNIST image detection
iv)The random number of batch size is also passed to network
v) The one hot encoding of argmax output of MNIST output is stacked with the one hot encoding of random numbers
vi)Then two fully connected layers are used to get the SUM with size 20.
vii) The network returns both MNIST and sum detection

#Training
i)loss1 is the MNIST detection loss and loss2 is the sum loss
ii) loss is taken as sum of loss1 and loss2
iii) The backward propagation is done on this loss
iv)As this is multi-class classification, cross_entropy is used.
v) Adam optimiser is used for grads upgrade
vi) The network and data is moved to GPU for training

#results
i) The training accuracy for MNIST image detection = 90%
ii) The validation accuracy for MNIST image detection = 87%
iii) The training accuracy for sum = 90%
iv) The validation accuracy for sum = 87%


