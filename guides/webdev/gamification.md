# Gamification and Web Development

## Introduction

Many websites utilize gamification to increase user experience, engagement, and overall interaction. For the users it’s fun and something that keeps them coming back. Implementing an effective gamification system can be more daunting than first imagined. 

In some simple scenarios, a ranking system based off points acquired is all that is necessary to get users to enjoy the system. Increasing the complexity in different ways from there can increase engagement even further.

On the other side of the equation if the gamification complexity is too much, the users will get confused or overwhelmed and won’t interact as much. Also if they think the system isn’t fair, too challenging, or too easy they will do the same. 

The trick is to find that fine line between challenging and forgiving. Knowing when to apply both and how to use the basic structure mechanics of a gamification system to get the desired results.

## Structure of a Gamification System

The various types of systems will be different in how they are structured. For this guide will be starting with a simple point system, level system, and combine that into a ranking structure. A foundation that can be expanded in a variety of ways depending on the desired result.

### Foundation

<img src="https://github.com/Triv2/writing/assets/126743500/fd0882a8-c59c-4f61-8f2d-bf0ab603c556" alt="leveling chart" width="300" height="500" />


### Values

This chart is from dungeons and dragon 5th edition leveling system. A perfect example from a system that has been tested by time.

1. **Points**

   > Known as experience points from the chart, are used to keep track of all the different interactions the user has done and the time invested into the application. Not all actions garner points, but any of the core mechanics of the system should give points.

  - The value for each interaction should directly correlate with time invested. But at the same time it needs to be even, meaning the same points should be awarded for the same task based on the average time it takes to complete the task.
  - If it takes one user 20 minutes and another 40 minutes, the points awarded should be the 	same. If the time to completion range is too large, the difficulty of the task should be 	examined to get a closer average time to completion.
  - Ideally points should be awarded for actions that increase engagement. 
  - Examples of this in web applications: posts, comments, reviews, uploads, shares, upvotes/downvotes, likes, replies, content creation, and event interactions.


2. **Level** 

    > This is summarized way to view the aggregation of points. It is also used as metric to determine a user’s progress and level of interaction with the system.
   
  - Can be seen as a status symbol for some users as a representation of the effort and time they have dedicated to the application.
  - Adding badges for different level brackets can help increase interaction as it gives users something to set as a goal.
  - Perks for different level brackets can help increase engagement as well. The perks should have a side effect of increasing engagement through interaction with the system or other users.

3. **Points to Next Level**

    > The amount of points required to progress to the next level. This amount can vary and should not follow a linear or exponential algorithm.
   
  - The reason being is if it is linear or exponential the difficulty of progression will either be too fast or too slow depending on how the algorithms are setup. 
  - The user shouldn’t level too fast or too slow, but move at a finely tuned pace that sets up the maximum amount of interaction and engagement. This will have to be tested through trial and error, analytics and other metrics to gauge the right values.
  - Another point to note is that setting the Points to Next Level as flat rounded up numbers in the hundreds and thousands are preferred. 
  - Psychologically humans prefer these numbers because of metric system and common use in society.
  - It is also easy to interpret and set as a goal.
  - Don't use static numbers for this value either such as every level you need 100 points, but you get less points per interaction as you level up. This feels like a treadmill to the user.


4. **Relative Percentage to Progress**

    > This tracks the variable change in the amount of points required to level over the course of the level system.

  - The relative percentage to progress from the chart shows a nice growth curve. The starting levels progress rapidly, first due to the base amount of points acquired from interactions and secondly the low amount of points required to progress to the next level.
  - Near the middle of the leveling range everything slows down more than it does at higher levels. Why? The leveling should follow a wave function so as to not be too easy or difficult. The middle ground will feel like a grind, but its setting the ton for the end levels.
  - The percentage increases but how long it takes to level may take longer because the base values for points awarded may not scale as well.

### Summary

As you can see the metrics involved in creating an enticing system can seem simple but have an underlying complexity. 
So far all we have noted is some characteristics of the variables attached to the system and how they work. 

In the next section we will break down an example of a bad gamification system and what we can do it improve it.

Something not covered in that chart that is worth mentioning is events. In a gamification system events are used to break up the monotony of leveling or grinding out levels for those that which to progress quickly. 
Events should also offer increased point rewards, unique cosmetic rewards, and be limited in the sense that they happen a few times per year or once in the system's lifetime.


## Applied Example

In this section we will use an example of an existing gamification system and go over it's limitations, it's flaws, and how we can improve them. 

It will also show a specific use-case to give you an idea of how it works for a specific platform and how to improve it. Keep in mind gamification is always evolving and can always be improved.

The goal isn't to make a one-size fits all best use case solution for web applications. It's to understand the basic underlying system and how to leverage that increase web application engagement and interaction.

Also how to apply these different methodologies in various applications.


### Example

** IN PROGRESS **

