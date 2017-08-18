# Simulated enviroment for Unmanned Surface Vehicles (usv_sim) -- 0.0.0
This simulator uses a combination of multiple physics packages to build a test enviroment for Unmanned Surface Vehicles (USV). We curently use UWsim for water surface modeling and ... . Our goal is to build a simulator for distater scenarios, such as floods, ... . We'll use it, at first, to develop and test control and trajectory strategies for USVs. but it can be easily adapted to other applications. It contains some robot models such as propeled boats and sailboats. You can find their xacros in packacge usv_sim.

## Getting Started

The main files to configure your simulations are:

1. XML files located into folder scenes of package usv_sim. In those files, you can configure UWSIM to run water simulation and some other world properties (current, waves and wind).
2. Launch files located into folder launch of package usv_sim. In those files, you can configure gazebo to run the simulation.
3. Xacro files located into folder xacro of package usv_sim. In those files, you can define the structure of your robot. You can use the available models (diferential boat, rudder boat, airboat and sailboat) as template to build your own model.

### Prerequisites

You need Linux 16.04 since the curent version of this simulator uses ROS Kinetic.

### Installing

1. cd ~/usv_sim_lsa
2. catkin_make_isolated --install
3. source ~/usv_sim_lsa/install_isolated/setup.bash
4. launchs:

    4.1 for heading control:   
        `roslaunch freefloating_gazebo_demo barco_ctrl_heading.launch`  
        `publish the desired location on topic /barco_auv/usv_postion_setpoint`  

    4.2 for velocity control:    
        `roslaunch freefloating_gazebo_demo barco_ctrl_vel.launch`
        `publish the desired location on topic /barco_auv/cmd_vel`  

    4.3 for differential boat with user interface to define joints positions:  
        `roslaunch usv_sim boat_diff.launch parse:=true`  
        `roslaunch usv_sim boat_diff.launch parse:=false gui:=true`  

    4.4 for differential boat with heading control:  
        `roslaunch usv_sim boat_diff.launch parse:=true`  
        `roslaunch usv_sim boat_diff.launch parse:=false gui:=false`  

    4.5 for differential boat with user interface to define joints positions:  
        `roslaunch usv_sim boat_rudder.launch parse:=true`  
        `roslaunch usv_sim boat_rudder.launch parse:=false gui:=true`  

    4.6 for rudder boat with heading control:  
        `roslaunch usv_sim boat_rudder.launch parse:=true`  
        `roslaunch usv_sim boat_rudder.launch parse:=false gui:=false`  

    4.7 for sailboat with user interface to define joints positions:  
        `roslaunch usv_sim sailboat.launch parse:=true`  
        `roslaunch usv_sim sailboat.launch parse:=false gui:=true`  

    4.8 for sailboat with heading control:  
        `roslaunch usv_sim sailboat.launch parse:=true`  
        `roslaunch usv_sim sailboat.launch parse:=false gui:=false`  

    4.9 for airboat with user interface to define joints positions:  
        `roslaunch usv_sim airboat.launch parse:=true`  
        `roslaunch usv_sim airboat.launch parse:=false gui:=true`  

    4.10 for airboat with heading control:  
        `roslaunch usv_sim airboat.launch parse:=true`  
        `roslaunch usv_sim airboat.launch parse:=false gui:=false`  

## Running the tests

TODO

## Contributing

TODO

## Versioning

TODO

## Authors

* **Alexandre Amory**
* **Davi Henrique** 
* **Marcelo Paravisi** 

## License

TODO

## Acknowledgments

* freefloating_gazebo
* UWsim
* LiftDrag 
