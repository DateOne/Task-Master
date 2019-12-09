# Task Master
The goal of task-master model is to **discrimitively** train an **ensemble** of neural networks, each of which is responsible for a sub-distribution of the dataset, so that during evaluation,
meta-tasks can be evaluated in more related models (according to **calculated relationship**) (or just tested on all models).
### Problems
* you want to you ensemble to learn multiple distributions with each modle in charge of its own. However, what don't just train each model on selected classes?\
A: That is a stupid question.
* How do you conduct such discrimitive training?\
A: find some hyper-parameters of structures for different models so that models can automatically be changed to be suitable to certain distribution.
* Why do you think this algorithm will work?
* If you just want to have an ensemble of different distributions and considering the existence of certain hyperparameters (like temperature) that can change models directly, why don't just 
get the best model, change hyperparameters and test with them? I know this sounds stupid and so similar to fine-tune the hyperparameter but normally, the best hyperparameter will be good for
all testing domain yet in few-shot learning, different hyperparameters will be good for different meta-tasks.
* will the mothod discribed above work?\
A: This hyperparamter, temperature, still focuses on averaging stuff which means its correlation with task relationships will be small, yet still worth a try. And we are still seeking for other
hyperparamters.
* What are the optimal hyperparameters?\
A: The optimal hyper-parameter is simple, that can emphasize certain little distributions yet the overall distribution can't be neglected.
So we might still need training. Over fitting on certain tasks? This might be inaccurate. So I'm gonna say, instead of overfitting, I say it dispatched interference. Are you talking about 
doing something on the dataloader part? That could be an idea.


experiment 1: see the power of temperature
experiment 2: explore other hyperparameters (better relates to little distributions)
