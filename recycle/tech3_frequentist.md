---
hide:
    - feedback
comments: true
---

# The Frequentist Approach
**: A quick note on intuition behind the frequentist approach of statistical inference.**

***Aug 4, 2023***

When starting out as a data science business consultant, fresh out of undergrad, my first manager asked me on my second day at work, do you know what a p-value is? 

I knew what it was, by definition, but I can say honestly that the intuition behind it escaped me at the time. With time I have seen much application of statistical inference in industrial settings. I feel like I’ve developed a better understanding of it.

I want to quickly walk through the frequentist approach along with the reader as a sort of revision. Let us think about the problem of statistical inference in figuring out if a hypothesis could have some truth.

Say we have an experiment with a treatment and a control group. We want there to be some significant change in a metric we are measuring between the two groups.

At the end of the day, we want to know if a change in that metric is worth our attention. This will establish the basis of our hypothesis. So now the million-dollar question is, what can we make of our observations after conducting the experiment? Does the data we observe sufficiently support our hypothesis or not? 

The Bayesian way of thinking would be, I can find a probability describing how likely my hypothesis would be true based on our observations in the experiment.

The Frequentist way of thinking would be, I can find a probability describing how likely the observations that I got would be as they are or more extreme if my hypothesis were true.

Both ways allow us to draw some conclusions about our observed data. They both make inferences about samples, quantify uncertainty and test hypotheses.

The strength of a Bayesian approach to this is that we can use what we already know to make better predictions (insert concept of priors and posteriors). The downside is that it could be computationally intensive for larger data. It could also lead us down a path of subjectivity where we make decisions about what could be before we see the actual data.

The strength of a Frequentist approach is that the results depend solely on the data without any need to think about specifics before seeing the data. It can be implemented in many scenarios for large amounts of data. Though the issue with this approach is that you’re not given a straightforward probability about how likely your hypothesis could be true. This could break the intuitive understanding and make interpretation challenging.

After the experiment, we found a slight change in the metric between the treatment and controls groups. We calculate a test statistic using the observed data. We would compare this test statistic with the test statistic if there really was no change in the metric. 

We use this comparison to find out the probability of seeing results as extreme as what we observed, or even more extreme, just by random chance. 

If that probability is very very low then we say that there isn’t much chance that we saw these results by fluke. This would indicate that there is significant evidence against the idea that there is no difference in the metric between the treatment and control. If that probability is not that low, then we would say there’s not enough evidence to say that there is no difference in the metric between the two groups. That probability is the p-value.
