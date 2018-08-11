# Udacity CarND Term 2, Project 2: Unscented-Kalman-Filter

## Project Basics
In this project, C++ was used to write a program taking in radar and lidar data to track position using Unscented Kalman Filters.

Predictions are made based on the sensor measurement which then updates the expected position. The primary C++ files making up this project are in the 'src' folder.

## Build instructions
Assuming you have 'cmake' and 'make' already:
1. Clone this repo.
2. Make a build directory: `mkdir build && cd build`
3. Compile: `cmake .. && make`
4. Run it: `./UnscentedKF` along with the Term 2 simulator.
   
## Initialization paramaters
It was neccessary in this project to tune various initialization parameters to improve the final calculated RMSE (root mean squared error). In the `ukf.cpp` file, the `std_a`, `std_yawd` were tuned.

* `std_a_`: process noise standard deviation longitudinal acceleration in m/s^2, was set to a value of 1 since the bicycle that was tracked in the project has low accelleration.
* `std_yawd_`: process noise standard deviation yaw acceleration in rad/s^2, was set to .3 radians.

## Results
Based on the provided data set, my Unscented Kalman Filter will produce the below results. The x-position is shown as 'px', y-position as 'py', velocity in the x-direction is 'vx', while velocity in the y-direction is 'vy'. Residual error is calculated by mean squared error (MSE).

| Input |   MSE   |
| ----- | ------- |
|  px   | 0.0761 |
|  py   | 0.0832 |
|  vx   | 0.3171 |
|  vy   | 0.2913 |


