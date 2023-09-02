# Franka-Emika-Panda-Robot-Arm-Inverse-Kinematics-Solver-Simulation-and-Hardware-Implementation
In this repository, you'll find code implementing inverse kinematics for Panda robot arm. Achieve accurate joint angle calculation using end effector pose. Rigorously tested in simulations and hardware for reliable performance.


# Panda Robot Arm Inverse Kinematics Solver

This repository presents my solution to the inverse kinematics problem for a simplified 6-DOF Panda robot arm. The goal is to determine joint angles that position the end effector accurately in a given pose. The code, housed in `calculateIK6.py`, computes feasible joint configurations, accommodating joint limits and ignoring self-collision.

## Methods

I devised a comprehensive strategy based on the Denavit-Hartenberg (DH) parameters and coordinate transformations. The DH parameters were obtained from the Panda arm's geometric properties. I calculated the transformation matrices between consecutive joints using DH parameters and formulated the end effector's transformation matrix relative to the base frame.

![image](https://github.com/Saibernard/Franka-Emika-Panda-Robot-Arm-Inverse-Kinematics-Solver-Simulation-and-Hardware-Implementation/assets/112599512/4657252e-8485-45e8-90dd-1b11a2048de5)

![image](https://github.com/Saibernard/Franka-Emika-Panda-Robot-Arm-Inverse-Kinematics-Solver-Simulation-and-Hardware-Implementation/assets/112599512/e4c0412c-fdf7-4ec1-94ff-f66d88bd9a55)

### Joint geometric analysis:

#### Joint 7: 

![image](https://github.com/Saibernard/Franka-Emika-Panda-Robot-Arm-Inverse-Kinematics-Solver-Simulation-and-Hardware-Implementation/assets/112599512/621f5e3c-de2e-44ff-94b2-c2277ecd59da)

#### Joint 5,6,2 (consideirng planar representation) :

![image](https://github.com/Saibernard/Franka-Emika-Panda-Robot-Arm-Inverse-Kinematics-Solver-Simulation-and-Hardware-Implementation/assets/112599512/660e6abe-3359-4339-a577-6f1065ff9630)


## Evaluation

The implementation underwent rigorous testing in both simulation and hardware. In simulation, I validated the joint angles output for various end effector poses against expected results. Hardware experiments were conducted, focusing on reachable workspaces and feasible orientations. Comparing simulated and hardware results provided insights into accuracy and limitations.

## Analysis

The analysis reveals notable consistencies between simulation and hardware outcomes. Certain orientations within the reachable workspace couldn't be achieved due to mechanical constraints. Deciding among multiple solutions for the IK problem was tackled, considering factors like joint angles' order and physical feasibility.

### End effector joint angle constraints:

![image](https://github.com/Saibernard/Franka-Emika-Panda-Robot-Arm-Inverse-Kinematics-Solver-Simulation-and-Hardware-Implementation/assets/112599512/031dfa0d-be7e-4d34-9289-dbcd11e16834)


## Contributions

This project contributes a reliable inverse kinematics solver, useful for controlling the Panda robot arm in various applications. The accompanying report provides insights into the solver's performance, offering a comprehensive evaluation approach.

## Usage

To utilize the code, import the `IK` class from `calculateIK6.py`. Provide the desired end effector pose (rotation matrix and translation vector) as input, and the code will return feasible joint angles. Joint limits and configurations are handled automatically.

## Acknowledgments

This project was completed as part of a robotics course assignment. The implementation draws inspiration from DH parameters and robotics kinematics principles.

## Future Work

Future enhancements could include extending the solver to handle more complex robotic manipulators and optimizing the solution for efficiency.

## Disclaimer

This repository was developed for educational purposes as part of a coursework assignment.

Feel free to explore the code, run simulations, and delve into the accompanying report for a detailed understanding of the implemented inverse kinematics solver for the Panda robot arm.
