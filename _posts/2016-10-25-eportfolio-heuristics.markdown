---
layout: post
title: 'E-Portfolio - Heuristics'
date: '2016-10-25 00:00:00'
---

*This post was part of my final semester e-portfolio: a linked series of posts on a common theme*

Being faced with complex decisions and problems is often a paralysing experience. The sheer size of the information to consider can often lead to *paralysis by analysis*. 
I found the concept of a heuristic, an information processing short-cut, liberating in that it removed the pressure to fully consider all the information when making a decision. 
At a more general level, it helped me appreciate that simplicity can be good when solving problems or making decisions.

I first came across the concept of heuristics in a Computer Science class, CS3243: Introduction to Artificial Intelligence (AI). 
A heuristic was an easily observed attribute or function of the system which could serve as an indicative factor to base decisions on. 
In other words, this means that the state of the world, often too vast or too difficult to encode as data, often has a more easily computed 'good enough' representation.  which does not reduce the optimality of the decisions made by the AI.

Heuristics were the bread and butter of AI programming for a long while as computers had too little processing power to encode the complete data for most problem domains. In my [project](https://drive.google.com/file/d/0B9ft2Ua3ZkxQT0xNRXFTNmN5R1U/view?usp=sharing) for this course, my group built an AI to play the popular arcade game Tetris. Tetris involves placing tiles falling into a shaft so as to form consecutive lines - see [Wikipedia](https://en.wikipedia.org/wiki/Tetris#Gameplay) for more. Our AI relied on a combination of 8 heuristics to decide how to play each piece. The snapshot of the source code below shows that the decision making factor, the *weightedScore* is the sum of 8 heuristic scores (underlined in the code excerpt below). These scores are based on easily observed attributes - for example, the *landingHeightScor* scores how many rows high the Tetris tile is when it lands. In this way, complicated decisions about which move to make, which might have to be based on a full understanding of the current and predicted board states, are approximated by picking the move that maximizes this score.

![Tetris Agent Code Extract](https://blog.nus.edu.sg/mohanjishnu/files/2016/10/Capture-pm39ms.jpg)
*A code extract from a Tetris Agent. The individual heuristic scores are underlined in red. Full code [here](https://gist.github.com/JishnuM/8824af83058993853a828ac1f0ca3a98)*

This proves extremely expedient in many cases, even beyond game-playing. In the presence of certain mathematical properties, using such simple heuristics can be proved to lead to optimal solutions. Therefore, in some cases, there is no cost to basing decisions on simple factors.

At this stage, while I fully appreciated the power of heuristics in computation, it took an USP course (UBH2209: Polycentric Governance) to understand its broader applications. One of the themes explored in this course was problem solving in complex situations. 
This had clear echoes of the computational problems discussed above - similar to the AI case, real world situations often had too many variables and possibilities to fully consider. 
Heuristics are introduced as a means of *fast and frugal*  decision making (Gigerenzer) which allows faster reaction with less information. A concrete example of such a heuristic is 'Take the Best', where cues are considered only one at a time when making decisions. 
For example, when comparing two houses, a Take the Best heuristic could first compare the number of rooms, and only if they are equal compare the floor area, and only if they are equal, the location, and so on. 
Therefore, additional information is sought only when the initial information does not enable making a decision either way. Surprisingly, eliminating information when making decisions in such cases proves not only convenient and easier but also to better outcomes. In environments where there is a large susceptibility of noise (i.e information which is usually not really relevant to the decision at hand), filtering out this unnecessary information leads to more accurate decisions.

A further insight through the course was that, at least loosely speaking, a good heuristic did not have to be a piece of information or a cue but could be a simple process.  In an essay submission for the course, excerpted below, I point out how the management theory concept of 'best practices', referring to the established procedure followed for a certain problem, is similar to a heuristic.

> The notion of best practices is very strongly linked to one vision of Gigerenzer’s heuristics, where focusing on a subset of key factors or cues is the most efficient strategy in a highly structured and stable environment.
> > Full essay [here](https://drive.google.com/file/d/0B9ft2Ua3ZkxQMUlyQUJ6S2RvdEk/view?usp=sharing)

Essentially, in many business environments, problems have certain essential characteristics or facets which need to be tackled and standard methods to tackle them. Focusing on information or procedures outside these standards is superfluous.

These courses have highlighted that often, in information-dense situations, **simplicity is good**. This can hold true in both technical domains, like AI, or in non-technical domains, like management. 
Situations or problems can possibly be understood well enough through only a few key attributes, and an urge to know more can even be counter-productive. 
As a learner, I will seek to keep reflecting on what value any new knowledge I gain is adding, and whether than knowledge is actually useful for my ends. After spending so much time as a student on analysis, divining copious insight from relatively little information, this can be extremely counter-intuitive.

I could see how this spoke to my own experiences at my own internship experience in Expedia, an internet travel company. My project involved extending a system to automatically moderate hotel reviews to show on the web page. The system estimated the likelihood of each review being spam or not, and displayed it if it was unlikely to be spam. I had to extend the system, initially working with English and other European languages, to Chinese and other Asian languages.

![Hotel Review](https://blog.nus.edu.sg/mohanjishnu/files/2016/10/Capture-5-1rqpwja.jpg)
*This is what constitutes a hotel review on Expedia*

I was initially very intimidated by the problem as Asian languages are notoriously complicated to process automatically. Since words are not cleanly separated by spaces, finding separate words itself is a non-trivial task. This would only be more complicated for me as I did not speak Chinese, Japanese, or Korean, the main target languages for my project.

![Personal Notes](https://blog.nus.edu.sg/mohanjishnu/files/2016/10/Capture-4-21k2emz.jpg)
*Screenshot extract from my personal notes in the first week of the project*

However, this proved a needless worry. The separation between individual words for Asian languages proved relatively unnecessary, and the system worked well enough by just using characters as words. Quoting from my internship report:

> The approach for Asian languages is to handle each character as a separate ngram. Therefore, the unigram would consist of a single character while the bigram consists of a pair of characters. While the character is not analogous to the word, the results are fairly similar, causing only a small loss in accuracy.
> > Full report [here](https://drive.google.com/file/d/0B9ft2Ua3ZkxQdlB4STl6SDJtSDg/view?usp=sharing)

This allowed me to bypass a time consuming and difficult step of finding a piece of information which would have added relatively very little value. The decision to continue with the simple, easily available data allowed me to complete the project successfully.


The topic of heuristics is also interesting to me beyond just its personal applicability. It is curious to consider how further progress in AI can better inform and elucidate how we ourselves work as 'learning machines', as well as how our ideas of how we learn and do seep into the styles of learning and action we encode in machines. Further developments and breakthroughs in AI can lead to more insightful learning or management theory, and we can look to these rich fields for clues on what paths to explore for AI. These junctions of knowledge promise to be fertile grounds to explore our understanding of cognition.

*Course Artifacts Mentioned:*

  * CS3243 [Project Prompt](https://drive.google.com/file/d/0B9ft2Ua3ZkxQT0xNRXFTNmN5R1U/view?usp=sharing), [Source Code](https://gist.github.com/JishnuM/8824af83058993853a828ac1f0ca3a98)
  * UHB2209 [Paper 2](https://drive.google.com/file/d/0B9ft2Ua3ZkxQMUlyQUJ6S2RvdEk/view?usp=sharing)
  * CP3880 [Project Report](https://drive.google.com/file/d/0B9ft2Ua3ZkxQdlB4STl6SDJtSDg/view?usp=sharing)


*Read More:*

Heuristics are rather similar to **[models]({% post_url 2016-10-30-eportfolio-models %})** in that they help deal with information. Models conveniently organize information in order to ease processing, while using heuristics implies that much of the information is dropped.

Of course, in the real world, we often do not have to deal with all this information alone. Relying on **[communities]({% post_url 2016-10-31-eportfolio-communities %})** to work together is yet another option.