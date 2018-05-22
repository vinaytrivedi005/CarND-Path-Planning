# Path Planning

In this project I am defining path and generate trajectory which car should follow.

### Model

#### Prediction

In prediction step I am looking at sensor data of other cars and checking any car is too close to cause collision in same lane we are driving or if we decide to change lane if there is any car in that lane too close to cause collision.

#### Behaviour

Based on the prediction result, I am defining behaviour of the car. There are 5 behaviours as follows:

1. keep lane
2. Switch to left lane
3. Switch to right lane

If there is a car ahead less than 30m ahead, I am deciding to change lane or slow down. To change lane, I am checking if there is any car in that lane within 30m ahead or 10m behind. If there is a car within that distance, changing to lane change might result in collition so, I am deciding that lane change is not possible. If lane change is not possible, the car will slow down. If lane change is possible, It will switch to the fastest lane. Fastest lane is decided based on the speed car going ahead of my car in that particular lane.

### Trajectory

Based on the chosen behaviour I am defining trajectory that car will follow.
