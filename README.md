# RL_FinancialMarkets

What is RL?

- Technique to make a machine solve a task without supervision
- When a task is performed we go through a number of steps
- At each step, the state of the system changes
-  Based on the state, we make a decision
- We finally get a reward based on the success or failure of our decision chain



# Markov Decision Process

- Take action(A)
- Transition to State(S)
- Get reward(R)
- A policy() that define the set of actions

The reward we get determines our Value(V)


# Markov chain

If a restaurant serves Pizza, hotdog and burger.

But they serve only one per day, if they serve one today, they serve another tomorrow.

![Screenshot 2023-02-09 at 18 29 07](https://user-images.githubusercontent.com/29931071/223426751-34fb4545-31ac-4e5b-8631-9f5820423b29.png)

If they serve burger today, the probability that they will serve Pizza tomorrow is 0.6

While the probability that they will serve burger tomorrow is 0.2

The arrows are called weighted arrows.

The second is a self pointing arrow

Now here are all the possible transitions

![Screenshot 2023-02-09 at 18 35 40](https://user-images.githubusercontent.com/29931071/223426895-b696990f-c038-4d8b-91cb-a6cc9cbfb048.png)


This is a markov chain

The most important property of the markov chain is that the future state depends only on the current state.

![Screenshot 2023-02-09 at 18 37 35](https://user-images.githubusercontent.com/29931071/223427028-d4a75bb2-9e35-4392-bd61-1b03068c6b39.png)


The probability that n+1 step will be x, depends only on the nth step, not the complete sequence that came before n.

The second property is that, the sum of the weights of the outgoing arrows of any state is 1.



# Markov Decision Process

![Screenshot 2023-03-07 at 13 52 53](https://user-images.githubusercontent.com/29931071/223427521-445f87d7-565d-4761-ad8f-30d237e72916.png)


## States

- States represent every state that one could be in.
- So there are 12 different states in this grid.
- We can represent these states in their x-y coordinates e.g start state =1,1, the goal state = 4,4

## Model or Transition Model

- This is a function of 3 variables. 1 A state 2 An action 3 Another state = ```T(S, a, S’)```
- What this function produces is the probability that you would end up transitioning to S’, given that you were in state S and you took action ```A. = Pr (S’     | S, a)```

The model defines the rule of the game.

## Actions

- Four different decisions we could make are up, down, left and right and stay where you are.
- The things you can execute when you’re in a particular state.

The Markovian Property

1 It means that only the present matters
It means that our transition model from S to S’ only depends on the current state S

You can turn almost anything into a markovian process by making sure that your current states remembers everything that it needs to remember from the past

2 Things are stationary, it means the markov rules don’t change
The agent is obviously not stationary, the transition model is stationary.

## Reward
 
  The reward you get from a state tells you the usefulness of entering into that state


Policy

![Screenshot 2023-03-07 at 13 55 55](https://user-images.githubusercontent.com/29931071/223428346-61d4ae31-bd13-495e-bdcc-0ce422ee0e39.png)

State + Model + Action + Reward = A problem.

But the solution to a markov decision process is called a policy.

A policy is a function that takes in a state and returns an action.

The optimal policy is the policy that maximizes your longterm expected reward

It’s a function that tells you what action to take in any state you’re in.

https://www.youtube.com/watch?v=dkBZ9YKuOVA&t=73s







