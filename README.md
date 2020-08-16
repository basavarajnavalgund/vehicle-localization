# **Kidnapped Vehicle Localization with a Particle Filter**

### Objective
The Vehicle has been "kidnapped" and transported to a new location! Luckily it has a map of this location and 
a (noisy) GPS estimate of its initial location. Then the vehicle starts to move, in the meanwhile, it records 
the noisy sensor and control data. A real-time particle filter is implemented to localize the vehicle with 
 the sensor data.

In this project, particle filter will be given a map and some initial localization information (analogous to 
what a GPS would provide). At each time step my filter 
will also get observation and control data. 

**System Explanation**: 
* Inputs:
    * one map contains landmarks
    * one initial location (e.g GPS) in the very beginning with big uncertainty.
    * noisy landmark observations in each timestamp while vehicle is moving.

* Outputs: 
    * The **blue circle** (with an black arrow inside) is the real-time estimation of the vehicle's location 
      and heading orientation from the particle filter.

* Ground truth: 
    * The **blue car** is the ground truth of the vehicle, including position and heading orientation. 
    It is only visualized for comparison purpose.


## Code & Files
### 1. Dependencies & environment

* cmake >= 3.5
* make >= 4.1
* gcc/g++ >= 5.4
* uWebSockets: used for communication between the main code and the simulator.
    

### 2. How to run the code

1. Clone this repo.
2. Clean the project: `$./clean.sh`
3. Build the project: `$./build.sh` 
4. Run the project: `$./run.sh`
5. Start the [simulator v1.45](https://github.com/udacity/self-driving-car-sim/releases), 
select the Kidnaped Vehicle, and click **start**. 


### 3. My project files 

* [CMakeLists.txt](CMakeLists.txt) is the cmake file.
* [data](data) folder contains sensor measurements, example images, GIF. 
* [src](src) folder contains the source code.
* [clean.sh](clean.sh) cleans the project.
* [build.sh](build.sh) builds the project.
* [run.sh](run.sh) runs the project.
* [install-mac](install-mac.sh) install uWebSockets in Mac.
* [install-ubuntu](install-ubuntu.sh) install uWebSockets in Ubuntu.


### 4. Code Style

* [Google's C++ style guide](https://google.github.io/styleguide/cppguide.html).



---

## System overview

![][image1]

[//]: # (Image References)
[image1]: ./data/1.png
[image2]: ./data/ekf_flow.jpg
[image3]: ./data/ekf_vs_kf.jpg
[image4]: ./data/lidar.jpg
[image5]: ./data/radar.jpg
[image6]: ./data/camera-vs-radar-vs-lidar_1.png
[demo_gif]: ./data/demo.gif
[lidar_gif]: ./data/lidar.gif
[both_gif]: ./data/both_lidar_radar.gif
