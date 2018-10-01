# navigation-control
Udacity Deep Reinforcement Learning Nanodegree Program - Project Submission About Navigation Control

Observations:

- To run the project just execute the <b>main.py</b> file.
- If you are not using the an windows environment, you will need to download the corresponding <b>"Banana"</b> version for you OS system. Mail me
  if you need more details about the environment .exe file.
- The checkpoint.pth has the expected average score already hit.
  
The problem:

- The environment solved here is a problem about navigation control where the agent must be able to navigate into an environment and
  collecting yellow bananas while avoiding the blue ones.
- For each yeallow banana collected it receives a +1 reward while when it collect a blue banana the reward is -1.
- The goal is get an average score of +13 over 100 consecutive episodes.

The solution:

- For this problem I am using an Double Deep Q-Learning with Memory Replay aproach.
- I have checked this approach along with prioritized experience replay but the results were almost the same whereas the performance
  decreased with the prioritized experience replay implementation due to the fact that the algorithm must be updating the error 
  value for all the memory buffer after each backward step. You can try it if you want but just changing the configurations of the 
  hyperparameters you can get the same results at the same scenery.
- The future goal is to use the Duelling Deep Q-Learning and check how it goes in comparison with the actual solution.

The hypeparameters:

  - The file with the hypeparameters configuration is the <b>agent.py</b>. 
  - If you want you can change the model configuration to into the <b>model.py</b> file.
  - The actual configuration if the hypeparameters is: ALPHA = 1, GAMMA = 0.99, TAU = 0.001, UPDATE_EVERY = 5, BUFFER_SIZE = 10000, 
    BATCH_SIZE = 300   
  - For the model there is just one hidden layer with input size and output size corresponding to the environment settings.