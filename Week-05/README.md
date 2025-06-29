# Week 5 : Thinking About Learning-Based Filling | SoC 2025 AnimAI Project

Now Week 05 is going to be more like a thinking exercise.
Feeding video frame node positions to an LSTM neural network is not a very trivial task. A very nice thought should go into it.

## If you haven’t yet…

Recently, We shared two good videos from **StatQuest by Josh Starmer**, explaining RNNs and LSTMs in a super clean way.

If you haven’t seen them yet, please go through them before trying to implement anything.

* [StatQuest: RNNs Clearly Explained](https://youtu.be/AsNTP8Kwu80?feature=shared)
* [StatQuest: LSTMs Clearly Explained](https://youtu.be/YCzL96nL7j0?feature=shared)

## Reference Implementations

The following two links show how to structure and train an LSTM for a numerical sequence task (they use stock prices, but the sequence-learning part is the same). You can adapt these directly for motion prediction by replacing prices with joint coordinates.

1. [Stock Price Prediction Using TensorFlow – GeeksforGeeks](https://www.geeksforgeeks.org/nlp/stock-price-prediction-project-using-tensorflow)
2. [How to Predict Stock Market Using LSTM – Medium](https://medium.com/@dmytrosazonov/how-to-predict-stock-market-using-google-tensorflow-and-lstm-neural-network-81ccc41a22a8)

## A Little Subtlety
We have covered how LSTMs work from a theoretical standpoint. We have seen that they can be used in a temporal fashion to predict something in the future based on past data. But our goal is not to predict something in the future, right?

Our goal is to find a **missing frame in between**, from the MoCap sensor data, which we already did completely with mathematical tools in Week 4.

Now the question is, **How do we feed this data to an LSTM?**, and even before that, **What data do we feed?**

Can we do something like:

* Feed the frames before the missing one and predict it like it’s in the future?
* Similarly, feed the frames after the missing one and predict it as if determining the past?

So can we do something like a **Bidirectional LSTM**? Which indeed finds the missing frame both from the future and past? Can we do that is what we are asking.

## So to formulate, two main problems:

1. **How will our neural network (suppose we are fixated on LSTM since we studied it) work?**
2. **How and what data are we going to feed to our neural network?**



## Our Background from Week 4

In Week 4 we worked with the **Human3.6M** dataset, in which we had **17 joints (nodes or keypoints)**, each of which had **x and y coordinates** in every frame.

The way we analyzed it back then was:
Look at each individual node moving across space and time (i.e., across frames).
So how do we now structure **this same data** to feed into the LSTM we are trying to build?

This is what you should sit and think about before jumping into the model.

## Suggested Exploration Setup

Try this basic framing to experiment with:

* Take 7 consecutive frames from your MoCap sequence just as we did in `Week-04`
* Remove or mask the middle one (frame `t`)
* Feed the 3 frames before and 3 frames after to the LSTM
* Train the model to predict the missing one

Do this repeatedly across the dataset, the model might start learning the motion pattern and structure, and fill in the missing frame based on the motion of all joints over time.

## Extension and Deeper Thought

Doing this will be **necessary** and **enough** for you to get your SoC 2025 certification. But we would recommend you to also do Part 3 and Part 4, which are optional. You can find them in the Week 4 final project problem statement at the following link:
[https://github.com/Yaswanth2747/SoC-AnimAI/tree/main/Week-04#final-project-problem-statement](https://github.com/Yaswanth2747/SoC-AnimAI/tree/main/Week-04#final-project-problem-statement)

We will add an outline for this Bidirectional LSTM implementation later on as part of `Week-06`. But do not rely on it at all. We want you to think about this problem carefully. We want you to convert what you have in mind into your own implementation and approach.

> Submission Deadline : `14 July, 2025 11:59 PM`

If you are interested, you can also explore mechanisms like attention. Until now, we have been filling frames for almost any kind of motion without caring about what the motion actually is. For example, whether the person is jumping, jogging, walking, or something else, our approach did not really take that into account. But the ability to predict the next frame as per the context, which attention mechanisms allow, is what lays the foundation for AI-based video generation.

Like ChatGPT, for example. It can predict the next word based on the overall context. A similar principle can be extended to videos, where the next frame is generated based on surrounding frames and the motion style being followed.

So this concludes SoC 2025 for you, and for us mentors. We thank you for being interactive and involved in this project. Thank you for trusting us. Always tell us where we can improve. 

# Thank you
Your Mentors and Friends,

Yaswanth and Harshith
