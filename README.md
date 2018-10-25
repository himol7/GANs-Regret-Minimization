# GANs-Regret-Minimization
Probabilistic future video frame prediction using Generative Adversarial Networks by employing a regret minimization strategy for training GANs.

As proposed by Ian Goodfellow in 2014, Generative Adversarial Networks are essentially two networks, a Generator and a Discriminator, pressed against eachother that learn from the opposite one's losses in a minmax game. 

## Generative Adversarial Networks:
![alt text](https://github.com/himol7/GANs-Regret-Minimization/blob/master/images/gans-diagram.jpg)
## Source: https://www.slideshare.net/ckmarkohchang/generative-adversarial-networks/11

minmax V(D,G) represents the min-max game between the Discriminator and Generator. Loss function used here: Log loss function.

## Regret Minimization:
![alt text](https://github.com/himol7/GANs-Regret-Minimization/blob/master/images/blockdiagram-w2.PNG)

## G: Generator
## D: Discriminator
## G-loss: Generator's loss
## D-loss: Discriminator's loss

For every iteration, D is supplied with G's output and D-loss is calculated. The D-loss for current iteration is propogated to next iteration where it is averaged with D-loss of that iteration and the mean loss is supplied to G for training it.

## Results:
![alt text](https://github.com/himol7/GANs-Regret-Minimization/blob/master/images/results.PNG)

G-loss converges significantly faster when averaged with previous losses.
