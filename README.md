In my project, I initially implemented a neural network architecture based on the 'handwriting.py' file from our 
lecture. This initial setup performed poorly with just a 5.3% accuracy rate. To improve it, I began tweaking various 
components of the model.
First, I adjusted the dropout rate, finding that reducing it to 30% led to a significant improvement, increasing 
accuracy to 91.7%. Further lowering the dropout rate to 20% yielded even better results at 92.3%, and 10% dropout 
pushed the accuracy to 94.3%. However, a dropout rate as low as 5% caused over-fitting.

I then experimented with the number of neurons in the hidden layer. Doubling it from 128 to 256 resulted in a modest 
accuracy increase from 92.2% to 95.0%. Surprisingly, adding another hidden layer with 128 neurons performed poorly 
at 82.5%.
Shifting focus to the convolutional and pooling layers, I added a second convolutional layer with 32 filters and a 
second max-pooling layer with a 2x2 pixel size. This change significantly improved accuracy to 97.6%. Other 
configurations did not surpass this performance.

Lastly, I attempted to combine the best-performing elements: 256 neurons, 2x convolutional layers with 64 filters, 
2x max-pooling layers, and a 20% dropout rate. However, this model achieved similar accuracy as the one with 32 filters 
and 128 neurons while requiring much more training time. Consequently, I opted to submit the more efficient model with 
32 filters and 128 neurons, which offered a good balance of accuracy and training time.