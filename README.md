Identification and PID control of a nonlinear Continuously Stirred Tank Reactor (CSTR) in Matab GUI environment.

Objective: Identification and PID control of a CSTR process with primary and secondary control loops. 

How to run: Download the zip file. Open and run `CSTR.m'. In case of size incompatibility set your screen resolutions to 1680*1050.

General description: The CSTR process has two control loops: (i) primary and (ii) secondary. 
The primary loop is in charge of controlling the temperature of the product (shown on bottom right of the picture). 
The secondary loop is designed to control the temperature of the jacket. 
It is assumed that the secondary loop is already controller by a proportion controller and the control gains is known. 
The objective is to design a primary control (either P, PI, or PID) so that the temperature of the output follows desired set points. 

Step 1. Pulse test for System identification: To identify the system and fit a linear model (a first order plus dead-time) one should click on the 'Pulse Test& Fit model' menu. 
For this step, the secondary loop should be in the 'P only' mode, while the primary loop is in the 'open loop' mode.
Once 'Pulse Test& Fit model' is selected the parameters for a step input (pulse test) are asked. 
After the pulse test is done, some initial guesses for the first-order model fit is asked. 
The software does its best to come up with good initial parameters, so best practice is to leave the initial parameters as they are. 
The model is shortly shown on the screen. If the model is satisfactory the user can select yes. Otherwise, another pulse test and fit model may be required.

Step 2. Tuning controller parameters: Once a model is fit to the obtained data, click on the 'Tuning parameters' menu, where a variety of different methods are available 
to tune P, PI, and PID parameters. By selecting the desired method, controller parameters are computed and shown.
Then, one can change the primary loop mode from 'manual mode' to the selected controller and manually enter the computed controller parameters.

Step 3. Set point tracking: Now, one can enter the desired set point and evaluate the performance of the designed controller.
Simply set the set point below the system model, and click on the 'simulate' button.


What model is used for the CSTR process?

The model is given in 'cstr1.m'
