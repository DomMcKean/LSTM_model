# LSTM_model

## Abstract 
 How can we predict future manipulation force in order to plan low force trajectories for robotic manipulation of deformable objects?
 In this work, we propose a Long-Short-Term-Memory (LSTM) model with a novel approach to data management that is capable of efficiently predicting manipulation forces over long robot trajectories (1000 time-steps @ 10Hz), even when the manipulated object is physically constrained by multiple obstacles, and given only the robot's position data as input.
Experimental results show that manipulation forces from bending and pulling long flexible elastic objects through and around obstacles can be efficiently modelled in only 40 minutes using an LSTM network and only a modest amount of training data.
 The results of this work will benefit areas of industry that still heavily rely on human workers to install long complex objects such as wiring, hoses and seals which can be easily damaged if not handled carefully. 
 
## 1. Introduction 
During a separate study on industrial needs, it was found that here is a need, particularly in the automotive and aerospace sectors, to automate tasks that involve the threading of thin flexible objects in and around tight obstacles for assembly purposes. Examples of such tasks include fitting wiring harnesses to vehicle chassis, hydraulic hoses for braking systems and industrial plant, and pneumatic tubing for industrial automation systems. 

"In the UK alone, there are more than 30 automotive manufacturers building in excess of 70 models of vehicle. Together they produce Over 1.3 million cars and 78,000 commercial vehicles every year.”. 
Although already highly automated, the manufacture of these vehicles still requires humans to install these flexible objects and researches and manufactures have for a long time being looking for a way to automate this complex task.
The state of the art when it comes to installing such deformable linear objects or (DLOs) is to use humans. To date, only humans have the dexterity and foresight to robustly handle DLOs in industrial environments. The difficulty in automating these sorts of tasks arise from the complex nonlinear forces inherent within flexible elastic objects with near infinite degrees of freedom and complex contact dynamics between objects and their environment that are constantly in flux as objects are bend and twisted into place. 
Some of these objects can be easily damaged when pulled around obstacles such as sharp chassis members, and a robotic system will need to reason about how the DLO may become trapped or snagged when manipulated and what can be done to either prevent or remedy the snagging.  
 
Even humans can have problems with dynamic environments, but we are usually very good at resolving problems by leveraging on our prior experiences. 
By training a robotic agent with enough experience, could it solve unforeseen problems when manipulating complex objects? Determining these complex forces by hand mathematically is difficult, taking in to account the friction between different materials, the plastic and elastic properties of materials, multiple contact points, gravity, speed and acceleration. Luckily, humans do not need to consider such things in order to predict how a flexible object may behave in a given environment because of our experience. Having interacted with so many different objects and materials during our lives, we have built up an intuition for how certain objects behave when manipulated. 
Using past manipulation data, we may be able to teach machine learning models this same intuition for how bending and pulling forces change when objects are bent and twisted in and around obstacles. 

This work is a step towards autonomous manipulation of DLOs in industrial environments. We propose a new method of modelling the complex contact dynamics using only real-world robot position data and show how reasonable results can be obtained when interacting with a number of environmental obstacles simultaneously. 
