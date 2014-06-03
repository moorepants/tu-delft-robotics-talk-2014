Outline
=======

Impetus
-------

- We need better controllers for powered prosthetics
- Putting numbers on the control being used can open up new ways to quantify
  gait.

Problem
-------

- What control algorithms are actually used during walking?

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

Non-perturbed results

Indetification of "fake" data
-----------------------------

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
4. 


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
