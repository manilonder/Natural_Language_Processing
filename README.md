# Natural_Language_Processing
Neural network architectures can produce powerful computational models for natural language processing. Here, you will consider one particular model for examining sequences of words. The task is to predict the fourth word in sequence given the preceding trigram, e.g., trigram: ‘Neural nets are’, fourth word: ‘awesome’. A database of articles were parsed to store sample fourgrams restricted to a vocabulary size of 250 words. The file data2.h5 con- tains training samples for input and output (trainx, traind), for validation (valx, vald), and for testing (testx, testd). Using these samples, the following network should be trained via backpropagation:
<img width="566" alt="Screenshot 2023-01-23 at 15 17 46" src="https://user-images.githubusercontent.com/59516214/214037722-bc7a3a6d-b33f-4e22-809f-d855fe0236f7.png">
The input layer has 3 neurons corresponding to the trigram entries. An embedding matrix
R (250×D) is used to linearly map each single word onto a vector representation of length
D. The same embedding matrix is used for each input word in the trigram, without consid-
ering the sequence order. The hidden layer uses a sigmoidal activation function on each of
P hidden-layer neurons. The output layer predicts a separate response zi for each of 250
vocabulary words, and the probability of each word is estimated via a soft-max operation
<img width="122" alt="Screenshot 2023-01-23 at 15 18 15" src="https://user-images.githubusercontent.com/59516214/214037787-4f740299-50b1-492e-840d-04a9f2f28643.png">
