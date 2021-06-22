# PLC Project: 3-Floors One Elevator


## Objective
Design a three-floor elevator.

## Design Description
This design aims at creating a working elevator. This is a very effective solution when it comes to solving the transportation question in a relatively high building where stairs are not so efficient. The design’s building is made of three floors: Gf, 1st floor and 2nd floor.

![1](https://user-images.githubusercontent.com/86275885/122985609-c6359700-d374-11eb-8c89-b75722501a9f.png)
![2](https://user-images.githubusercontent.com/86275885/122985607-c59d0080-d374-11eb-8ce9-845fb6bbfc61.png)


Inside the elevator room there are 3 switches available placed on the wall each allowing the client to navigate to the respective floor. On the door there is a laser bean sensor which will detect any object in its pathway and give back a signal. If an object is detected the timer on the door will pause and the elevator doors won’t close until this object is removed from the pathway. It takes the elevator 5s to close its doors and 10s to move from one level to another whether moving up or down.

## Design Interface

### INPUTS
- I1 Down L2
- I3 Go 2nd
- I5 Weight
- I6 Sensor
- I7 Up L1
- I8 Down L1
- I9 Go 1st
- ID Up GF
- IF Go GF


### OUTPUTS
- Q1 Down 2
- Q3 Open 2
- Q4 Close 2
- Q5 Weight
- Q6 Sensor
- Q7 Up 2
- Q8 Down 1
- Q9 Open 1
- QA Close 1
- QD Up GF
- QF Open GF
- QG Close GF


## Design Logic
- When any of the outer buttons on each floor are pressed, the elevator will move and arrive to the corresponding floor to serve the client. 
- The elevator’s initial position is on the Ground Floor.
- When moving up the elevator will neglect any outer button command from Level 1 where the user wants to go downwards and same applies if the elevator is moving down and a user on floor 1 has commanded a button to go upwards to level 2.
- It takes 5s for the elevator doors to close on any level and 10s to move from one level to another. 
- Once the elevator reaches the final level which is level 2, all pressed buttons on the inside will be cleared. 


## Design State Machines

![3](https://user-images.githubusercontent.com/86275885/122985898-19a7e500-d375-11eb-9de1-5ef444ffd8d5.png)
![4](https://user-images.githubusercontent.com/86275885/122985903-1ad91200-d375-11eb-8f6e-2bfdb88f86f2.png)
![5](https://user-images.githubusercontent.com/86275885/122985904-1ad91200-d375-11eb-93da-aff30f8e9650.png)


## Conclusion
This project implemented a state machine which taught us how to create several state machines and implement synchronized jobs among them all and design a mechanism to link them. It allowed us to dynamically draw a pattern between the different situations and control them efficiently. 
