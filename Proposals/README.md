## Prototyping my ideas:

* Cockroach based heuristic search optimization algorithm.

---

## Reinforcement learning: A more subtle way of learning
Previously I mentioned that observing the trade-offs between punishment and reward based learning would be helpful in infering most optimal learning approach for an agent.  
A more `computational neuroscience` approach would be to introduce **Temporal coding** and  **Spiking neural network** methodologies.   
I would like to include the "punishment" or "pain" based parameters as nociceptive spiking response. EEGs recorded during the time of induced pain can be used to train the spiking network, since it wouldn't be so optimal to train a spiking neural network based on real time EEGs I would take temporal coding in account, generating and detecting acute pain signals can come handy in that case.  
Approach: 
>Learning Agent with a pain threshold $Pe$ --> Initialize environment $Ev$ with "obstacles"(anything which induces negative rewarding) --> Simulate the agent for set of generations and capture no.of $Pe$ reachs --> Initializing pain signals using temporal coding technique and train a SNN to detect the pain --> Create a function to minimize the pain(just like increasing reward using Q-learning table).
