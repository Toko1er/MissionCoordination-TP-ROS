# Mission_coordination lab , Done by JIOKENG I TOKO Jean Junior Maldini & MAHIR Cavvas, 2025
Simulating efficient and collision-free movement of multiple robots

# Objective
The goal of this project is to navigate three robots from their starting positions to their designated flags while:

Avoiding collisions with other robots.
Reaching their respective flags as quickly as possible.
Robot Specifications
Sensors: Each robot is equipped with an ultrasonic sensor (range: 5 meters) for obstacle detection.
Actuators: Two motorized wheels for movement.
Awareness: Real-time knowledge of their current position and orientation in the environment.
This simulation showcases multi-robot coordination and navigation techniques in a controlled environment..

# Approach
## 1. Time Delay Strategy

To ensure the robots move to their respective flags without collisions, a time-delay strategy is implemented. By staggering the start time of each robot, their movements are coordinated, reducing the risk of collisions.

Key aspects of the strategy:
Distance-Based Adjustment: Each robot continuously detects the distance to its assigned flag and adjusts its speed accordingly, stopping when the flag is reached.
Open-Loop Control: The solution does not account for changes in flag positions during execution, relying solely on the initial configuration.
While effective for static environments, this approach may fail in dynamic scenarios where flag positions change during the program's runtime.

## 2. Curve Avoiding

This strategy employs a combination of PID control and obstacle avoidance to navigate a robot to its designated flag in a simulated environment. The robot begins by calculating its distance to the flag and uses a PID controller to adjust its speed and direction dynamically based on positional errors and yaw angles including:

Obstacle Avoidance: The robot continuously monitors its ultrasonic sensor. If an obstacle is detected within a predefined range, the robot stops and adjusts its orientation to avoid collisions.
Distance-Based Adjustment: The robot reduces its speed as it approaches the flag to ensure precise stopping.
Proportional Control: The PID controller minimizes errors in distance and direction to ensure smooth navigation.
Open-Loop Behavior: While the robot dynamically adjusts speed and angle, the position of the flag is fixed throughout the execution. Any dynamic changes to the environment may reduce efficiency.

