# Ex.No: 11  Planning –  Block World Problem 
### DATE:07.10.2023	 			                                                                       
### REGISTER NUMBER : 212221220061
### AIM: 
To find the sequence of plan for Block word problem using PDDL  
###  Algorithm:
Step 1 :  Start the program <br>
Step 2 : Create a domain for Block world Problem <br>
Step 3 :  Create a domain by specifying predicates clear, on table, on, arm-empty, holding. <br>
Step 4 : Specify the actions pickup, putdown, stack and un-stack in Block world problem <br>
Step 5 :  In pickup action, Robot arm pick the block on table. Precondition is Block is on table and no other block on specified block and arm-hand empty.<br>
Step 6:  In putdown action, Robot arm place the block on table. Precondition is robot-arm holding the block.<br>
Step 7 : In un-stack action, Robot arm pick the block on some block. Precondition is Block is on another block and no other block on specified block and arm-hand empty.<br>
Step 8 : In stack action, Robot arm place the block on under block. Precondition is Block holded by robot arm and no other block on under block.<br>
Step 9 : Define a problem for block world problem.<br> 
Step 10 : Obtain the plan for given problem.<br> 
     
### Program:
```
(define (problem pb1) 
 (:domain blocksworld) 
 (:objects a b) 
 (:init (on-table a) (on-table b)  (clear a)  (clear b) (arm-empty)) 
 (:goal (and (on a b))))     
```
### Output:
![image](https://github.com/viswapriyaG/AI_Lab_2023-24/assets/131427787/a631c9e7-1bac-4103-851f-32539960b34e)




### Program 2:
```
(define(problem pb3) 
(:domain blocksworld) 
(:objects a b c) 
(:init (on-table a) (on-table b)   (on-table c)   
(clear a)  (clear b) (clear c) (arm-empty)) 
(:goal (and (on a b) (on b c))))
```

### Output:
![image](https://github.com/viswapriyaG/AI_Lab_2023-24/assets/131427787/adb3ffbe-a05b-4917-b2b6-b7cc50a79101)




### Result:
Thus the plan was found for the initial and goal state of block world problem.
