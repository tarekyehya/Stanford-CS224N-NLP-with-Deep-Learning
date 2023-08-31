Welcome to Assignment 3!

We'll be using PyTorch for this assignment. If you're not familiar with PyTorch, or if you would like to review some of the fundamentals of PyTorch, the PyTorch review session is posted on Canvas under Course Videos.  

If you want to continue using your cs224n environment from assignment 1 for this assignment, please make sure you have all the dependencies listed in local_env.yml. To do so, please run: 

# 1. Activate your old environment:

    conda activate cs224n

# 2. Install docopt

    conda install docopt

# 3. Install pytorch, torchvision, and tqdm

    conda install pytorch torchvision -c pytorch
    conda install -c anaconda tqdm


If you would like to instead create a new environment for this assignment, please run:

# 1. Create an environment with dependencies specified in local_env.yml (note that this can take some time depending on your laptop):
    
    conda env create -f local_env.yml

# 2. Activate the new environment:
    
    conda activate cs224n_a3
    

# To deactivate an active environment, use
    
    conda deactivate


implementing the dependency parsing transition with neural network depend on the original paper,
the framework split into two steps the first is the algorithm of transition dependency and the second in how to train a neural network to predict the next step in this algorithm depend on a data prepared with human,
The assignment has alot of challenges but I love to highlight this step,
Every sentence is an example to train, we need to store to every sentence a buffer, stack and dependencies,
and on every epoch of the Train the state of all these is changed,
the challenge that I want to highlight how to store these for every sentence, 
if we store all of them in a list of dictionary will be a good but every train the state for all ( batch or mini batch ) will changed and we need to treat with code with all thesis, 
but the best solution is make a class for the sentence and initialize the buffer, etc., and the methods needed to the algorithm ( make the changing in the state Esey ),
list if objects and the Train with pyTourch.


