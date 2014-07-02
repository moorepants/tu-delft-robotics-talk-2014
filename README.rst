This work is licensed under a `Creative Commons Attribution 4.0 International
License <http://creativecommons.org/licenses/by/4.0/>`_.

Outline
=======

Background
---------
- UCD and TU Delft
- Identificatin of human control in the bicycle control task
- Direct ID of the plant and indirect ID of the controller

Literature Review
-----------------

- Standing: lots of papers
- Gait: not so much...Rouse
- Identifciation of human systems: Kearney
- Reflexes during walking: electrical stimulation

Impetus
-------

- We need better controllers for powered prosthetics
- Putting numbers on the control being used can open up new ways to quantify
  gait.

Problem
-------

- What control algorithms are actually used during walking? Only human data can
  tell us.

The System
----------

- Show block diagram of generalized gait system (van der Kooij has a nice
  diagram)
- Feedback? preview? delays?

Closed Loop System Identification
---------------------------------

- Ljung 1999

  - Direct Approach: measure input/ouput to plant or controller
  - Indirect Approach: measure set point and closed loop output, known
    controller or plant to get
  - Joint Input-Output Approach: measure set point, plant input, and output

- Direct Approach can introduce bias
  - Noise model must be accounted for (Ljung 1999)
  - If extrenal perturbation are high enough relative to sensor noise, then the
    controller can be estimated

- Indirect Approach
- Joint Input-Ouput Approach

- Show some of Samin's results

Measurements
------------

- ground reaction loads
- marker location
- belt speed

Method
------

1. Compute inverse kinematics and dynamics to get estimates of the joint
   angles, rates, and torques.
2. Time domain direct identification
3. Linear least squares
4. Design matrix

Experiments
-----------

1. 3 speeds, 10+ subjects
2. Psuedo random variation in speed
3. 2 minutes unperturbed, 8 minutes perturb

Sample Measurements
-------------------
- belt speed
- ground reaction loads
- marker positions

Estimations
-----------
- joint angles, rates, torques

Compare perturbed to non perturbed

Gain Results
------------

- show gain plots
- show joint isolated results and full gain matrix (but just joint isolated
  gain entries)

Model Validation

Show that the unperturbed data gives similar results.

Show the vaf results for the just m*, K and full K

summary
zero gains in the swign phase
negative velocity gains do not make sense

How far have we moved in the direction for the impetus. Can we put these gains
in exoskeleton?

piecewise set points for the others

Indentification of "fake" data
------------------------------

Identification from Simulation
------------------------------

- direct collocation finds an open loop control solution
- add constant gain feedback to model and simulated under random perturbations
- show results of constant gain simulation

Problems
--------

Is it the plant dynamics

Future
------

- indirect identification

Optimal control approach

1. Choose controller structure(s)
2. Develop plant model
3. Simulate model under
3. Cost function: minimize error in marker pos


- Title
- Videos of exoskeletons walking (or prosthetic legs)
- An idealized control system used by the human during a gait cycle
- Control system of a lower limb powered exoskeleton
- Identification of the control system used in able bodied walkers
- Description of the sensors and actuators on a lower limb exoskeleton
- Gait phase scheduled controller
- External disturbances
- Forcelink treadmill
- Motion capture system
- Protocol
- Video of walker being longitudinally perturbed.
- Example measurements (estimatations) (variation in joint angles, rates, and torques)
- Fit plots
- Gain plots
- Discussion
- Announcement about tutorial


DW2014
======

- Is this a good way to design a feedback controller for walking?
- Present our idea
- Present other's methods
- Does perturabtion needed?
- Neural networks, time delays
- Have to big data, random pertrub
- Try to mimic
- Are we really optimal? Should optimal control be the solution or should we
  try to do what people do?
- zero moment point, simbicon
- How do people actually respond to pertrubations?
- An infinite number of controllers can produce the same jont and torque curves.
- Do robotos use k

TODO
- Move Mathjax lib into this directory

Introduction
------------

What kind of control do you we use in gait?
-------------------------------------------

- Zero moment point control: Asimo, etc
- Optimal control: maximize stability, minimize energy?
- Something else?
- What can data from able-bodied humans tell us about the control mechanism
  during gait?

What kind of experiments can tell us something about human control during gait?
-------------------------------------------------------------------------------

- Can we come up with a holistic controller that resembles what humans actually
  do, defects and all?

Our goal
--------

- We're interested in improving the natural motion of powered prosthetics
  and exoskeletons including addign balance.
- We'd like to collect data from human's during gait, use a data driven
  approach to generate control models
- If we replace a human's leg with a powered prosthetic, how can we make it
  behave like the leg it replaced without connections to the human's central
  nervous system?

Our Approach
------------

1. Collect lots of common gait data: many gait cycles
2. Apply external perturbations to the human
3. Assume a simple time varying linear MIMO control structure
4. Find the best fit of the model to the data

Let the data (and, of course, some hunches) tell us what the control mechanism is.

Model Structure

Show block diagram and the controller equations.

Show linear least squares slide.

Show video of walking on treadmill.

Show resulting gains and one model fit.

Other ideas:

- Indirect identification: assume plant model, identify the closed loop system,
  with controller as free parameters
- Other control structures? How complex do they need to be if we are only
  trying provide feedback for prosthetics? How complex for more basic
  understanding of the control system.
- What sensors are essential in a powered prosthetic to reproduce gait?
- Subsystem identification?
