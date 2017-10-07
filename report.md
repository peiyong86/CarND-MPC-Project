1, Student describes their model in detail. This includes the state, actuators and update equations.
Answer: The state include x position, y position, psi (the direction), v(the speed), cte(position error) and epsi(direction error).
update equation: ![im1](https://github.com/peiyong86/CarND-MPC-Project/blob/master/im1.png)


2, Student discusses the reasoning behind the chosen N (timestep length) and dt (elapsed duration between timesteps) values. Additionally the student details the previous values tried.
Answer: Copy the N and dt from lesson 19's pratice, which is 25 and 0.05
Then just simply try N = 20 for no special reason.
I think 25 should also work in my code.


3, If the student preprocesses waypoints, the vehicle state, and/or actuators prior to the MPC procedure it is described.
Answer: In preprocess I transfer the coordinate system of points from world coordinate system to car's local coordinate system.
So later I can directly use the returned points coordinate without transfer it.

4, The student implements Model Predictive Control that handles a 100 millisecond latency. Student provides details on how they deal with latency.
Answer: The project code provide this line:this_thread::sleep_for(chrono::milliseconds(100));
And also MPC model will predict future steps to give good result.

