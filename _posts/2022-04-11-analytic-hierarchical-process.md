---
layout: post
title:  "Benefits of the analytic hierarchical process"
author: Bruce R Graham
categories: [ operational research ]
---

![Rational choices!](/images/rational.jpg)

One of the most inspiring techniques I learnt as a student of operational research yonkers ago was a procedure called the analytical hierarchical process. It was invented by Saaty in 1980.

The miraculous AHP as abbreviated, I have used tidily ever since to work out the most rational ways forward when I have had very difficult or complicated decisions to make.

The AHP leads to a weighted result of the most important options in your decision and so, you can rank which option is most to least important.

However, there is some work to reaching a conclusion. Depending on your software this is harder or easier to do. You guessed it, the open source R statistical language has a library for AHP, and it simply involves writing a YAML formatted configuration of the model. This is actually quite an endeavour the first time but once you are used to the format of the configuration file you will be well away.

The procedure for modelling AHP is broken into several parts.

The first part is to decide on what the decision is to be made and then the types of choices you need to make. These choices, moulded with their alternatives forms the first part of the ahp modelling process.

In choosing a car (the decision) there are a number of choices to make. What make and model? The make may be a preference and each model has it's own specs like fuel consumption, engine capacity, size and comfort. Create a comprehensive list of all the choices with all the quantitative and qualitative information related to each choice.

Secondly, everybody involved in making the decision should be weighed according to their importance in the decision. Every individual involved in the decision needs to perform pairwise comparisons of the alternative choices. If there are lots of choices, this can become very cumbersome. But some shortcut methods to this problem have been developed.

The final step is to encode the information into a specially formatted configuration file which the AHP algorithm can process. The YAML (yet another markup language) format is quite simple and easy to understand. The domain specific markups take a little bit of getting used to, but once you know the way to structure the model the whole process is very easy.

The AHP algorithm yields a matrix of preferences per decision type. The perferences are a percentage showing the importance of each category to the decision. A final decision can also be reached and gives you an accurate idea of the choices you need to make to optimally make the decision.

As an example, [this](/assets/house4.ahp) is a model configuration to choose a house.

Running this model in R, a decision matrix is generated.

![Decision matrix](/images/decision-matrix.jpg)

This matrix, based on the pairwise comparisons of the decision makers, shows that LIGHT is the most important criteria in deciding on a new house for this decision maker. Further, HOUSE2 has the best light and overall it is the best house amongst the choices.

As you can see, the decision matrix that the R's AHP algorithm generates is easy to interpret and intuitive.

If you would like the author to create a model at your behest, please drop a line at bruceg72@pm.me to get a quote.



