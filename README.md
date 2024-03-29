# Time-series-forecasting-using-GRU

![image](https://github.com/FeresDarouich/Time-series-forecasting-using-GRU/assets/120333973/1845e557-9eed-406a-a8b2-9899b4db0f50)

# What is Gated Recurrent Unit(GRU) ?

GRU stands for Gated Recurrent Unit, which is a type of recurrent neural network (RNN) architecture that is similar to LSTM (Long Short-Term Memory).

Like LSTM, GRU is designed to model sequential data by allowing information to be selectively remembered or forgotten over time. However, GRU has a simpler architecture than LSTM, with fewer parameters, which can make it easier to train and more computationally efficient.

The main difference between GRU and LSTM is the way they handle the memory cell state. In LSTM, the memory cell state is maintained separately from the hidden state and is updated using three gates: the input gate, output gate, and forget gate. In GRU, the memory cell state is replaced with a “candidate activation vector,” which is updated using two gates: the reset gate and update gate.

The reset gate determines how much of the previous hidden state to forget, while the update gate determines how much of the candidate activation vector to incorporate into the new hidden state.

Overall, GRU is a popular alternative to LSTM for modeling sequential data, especially in cases where computational resources are limited or where a simpler architecture is desired.


# GRU Architecture
The GRU architecture consists of the following components:

# Input layer: 
The input layer takes in sequential data, such as a sequence of words or a time series of values, and feeds it into the GRU.
# Hidden layer:
The hidden layer is where the recurrent computation occurs. At each time step, the hidden state is updated based on the current input and the previous hidden state. The hidden state is a vector of numbers that represents the network’s “memory” of the previous inputs.
# Reset gate:
The reset gate determines how much of the previous hidden state to forget. It takes as input the previous hidden state and the current input, and produces a vector of numbers between 0 and 1 that controls the degree to which the previous hidden state is “reset” at the current time step.
# Update gate: 
The update gate determines how much of the candidate activation vector to incorporate into the new hidden state. It takes as input the previous hidden state and the current input, and produces a vector of numbers between 0 and 1 that controls the degree to which the candidate activation vector is incorporated into the new hidden state.
# Candidate activation vector:
The candidate activation vector is a modified version of the previous hidden state that is “reset” by the reset gate and combined with the current input. It is computed using a tanh activation function that squashes its output between -1 and 1.
#Output layer: 
The output layer takes the final hidden state as input and produces the network’s output. This could be a single number, a sequence of numbers, or a probability distribution over classes, depending on the task at hand.
# Pros and Cons of GRU #
Like any machine learning model, Gated Recurrent Unit (GRU) neural networks have both advantages and disadvantages. Here are some pros and cons of using GRU:

# Pros:

GRU networks are similar to Long Short-Term Memory (LSTM) networks, but with fewer parameters, making them computationally less expensive and faster to train.
GRU networks can handle long-term dependencies in sequential data by selectively remembering and forgetting previous inputs.
GRU networks have been shown to perform well on a variety of tasks, including natural language processing, speech recognition, and music generation.
GRU networks can be used for both sequence-to-sequence and sequence classification tasks.
# Cons:

GRU networks may not perform as well as LSTMs on tasks that require modeling very long-term dependencies or complex sequential patterns.
GRU networks may be more prone to overfitting than LSTMs, especially on smaller datasets.
GRU networks require careful tuning of hyperparameters, such as the number of hidden units and learning rate, to achieve good performance.
GRU networks may not be as interpretable as other machine learning models, since the gating mechanism can make it difficult to understand how the network is making predictions.
