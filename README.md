# Simulation-based game testing for estimating player curiosity
Master thesis project


For instance, it would be interesting to train an agent to play Mario using Unity Machine Learning agents,
(e.g., using this one: https://github.com/linhdvu14/SMB-clone) and create levels that have clearly different amounts of novelty and complexity. 
You could then have humans play the levels and rate their curiosity towards the game, a
nd try to predict that with the self-supervised AI curiosity mechanism implemented in Unity Machine Learning agents.
The title of the thesis could be “Predicting player curiosity using AI playtesting”


About how to rate human curiosity: There are psychological questionnaires for that, which you should have players answer after each level. The data is noisy, which means we need many players. Thus, best to make a webgl build of the game (easy in Unity) and recruit players to play and answer questions in a browser. You should also read some psychological basics, e.g., https://www.google.com/books?hl=en&lr=&id=hNShDwAAQBAJ&oi=fnd&pg=PA157&dq=silvia+curiosity&ots=i7rDh1FFmn&sig=P-OZBnpr496d_UkuMnIzUgBhnTw

the curiosity ratings of the players should be implemented as questionnaire questions answered after each game level. The levels should be presented in different random order to each player. The AI curiosity mechanism is this one: https://blogs.unity3d.com/2018/06/26/solving-sparse-reward-tasks-with-curiosity/, based on this paper: https://pathak22.github.io/noreward-rl/resources/icml17.pdf. You should look at the Unity Machine Learning Agents code and log the curiosity reward for each timestep. We can then try different things like computing the average value and training a linear model that predicts human curiosity ratings as human=a*average(agent_curiosity_reward)+b.


Short and informational article on how to structure your thesis and tell a coherent story:

https://blogs.aalto.fi/writingaboutdesign/2020/10/27/writing-a-good-storyline-for-a-thesis-or-an-article/

More comprehensive set of info, including many example theses:

https://wiki.aalto.fi/pages/viewpage.action?spaceKey=AaltoHCI&title=How+to+Write+a+Great+Master%27s+Thesis+on+Human-Computer+Interaction%3A+Tips+and+Best+Practices
