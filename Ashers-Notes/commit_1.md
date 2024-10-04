
> # https://www.youtube.com/watch?v=aircAruvnKk
> ## Video 1:
> 
> Neuron – Thing that holds a number.<br>
> The number inside the neuron is from 1-0 and it is called the activation. It represents how much the shown number looks like a possible number type.
> Different layers in the network correspond to different parts of a number.
> Each neuron is assigned a weight as it travels to a new neuron to a new layer. This weight is a number and you sum all the (activation*weight) terms to highlight a region on an image grid you want the next neuron in the new layer to focus on. Basically, from all the inputs, ones with low weights (not related to the region the next neuron is assigned to) get dissolved out.
> So that’s cool and all but a weighted sum spits out a large number line so we put it in a sigmoid function to squish it down (just use multiplication to squish the numberline down to 0-1).
> Ok well baby you don’t want ZERO to ONE but some other range for the neuron to be able to light up. We call the accepted weighted sum range the neuron’s BIAS.

> TL;DR:
> Weight = What pixel pattern is the new neuron looking for?
> Bias = How strong must the incoming signal be to activate the neuron?

 

> # https://www.youtube.com/watch?v=IHZwWFHWa-w
> ## Video 2:
> 
> Cost function is how a machine learns. It sees how badly it performed: It works by adding up the squares of all the output neuron values and what they should be in an ideal world (you already know the answer to what you gave the machine for this stage). You sum those differences and get the cost. Obviously, when the cost is low, that means the machine is working near-perfect.
> Alr great, but how will it get better: If the cost function were graphed, to get to a min point you want to take the steepest way down. So, take the negative gradient of the cost. Tip: Make step sizes proportional to slope so as you get closer you get more precise with adjusting each iteration of the neural network.
> 
> Something super cool is that the ACTUAL way the neural network works is by analyzing a hodge-podge mess of pixels representing traits of the whole image thousands of times. In other words, while it can give hits, it cannot give correct rejections. It gives confident, nonsense, answers. It’s like: Haha, the computer can’t draw. It cannot say no, it cannot do anything other than what it was told which implies its initial input IS a number.

 

> # https://www.youtube.com/watch?v=Ilg3gGewQ5U
> ## Video 3:
> 
> Backpropagation is how we compute the steepest descent:
> When it comes to honing-in on the lowest cost, changing a large weight value will have a larger effect than changing a small weight value.
> Look at outputs from Neural Network and how it compares to expected values. Activations that are close to expected values should be nudged a little bit and activations that are super far should be nudged a lot (either up or down)
> For each output neuron, three ways to modify its output: Change bias, change weights, change previous layers’ activations. See how the other layer’s neurons ought to change (up or down and by how much based on how far each is from its desired value) and do ALL this for EACH individual neuron in the output layer. (see adding up and down arrows at 7:55)
> Changing weights of neurons with high activations also has a larger effect than weights of neurons with low activation / changing activation of ones with weights vice versa.
> Basically, go layer by layer backwards up the neural network, from ass to head, and see what is the desired change for each neuron in the layer to then find the needed nudges to make those nudges in the layer before THAT to see what is the needed nudges to make… ect. Sum the nudges together somehow and you get the net tweak for ur output activation values. That is what we’re doing, but not HOW we do it, that takes a lot of math.
> Doing this backpropagation for many many many different images is what is actually training the network. This is done by recording the desired changes of each component of the neural network for every trial and then averaging the changes per component. I.e. trial 1 says change W12 by +8, and trial 2 says change W12 by -5, so on and so on, so 8-5+.../n is the net change you should make for that one weight.
> Funnily and cool enough, putting all the changes in a column vector gets you the negative gradient of the cost function. Or at least something proportional.
> THIS IS ALL SWAG EXCEPT ITS SO MUCH MATH SO WE DO SOMETHING SIMPLER INSTEAD.
> Randomly shuffle activation data for all the numbers u fed the machine.
> Divide into sections, i.e. 100 groups of activations per section.
> Find avg of that, that is a good approx of the steepest descent.
> Avg all those avgs (maybe)
> Or just prolly take each one of those steps sequentially
> This is called Stochastic Gradient Descent.

  

> # https://www.youtube.com/watch?v=tIeHLnjs5U8
> ## Video 4:
> HIIIII
 