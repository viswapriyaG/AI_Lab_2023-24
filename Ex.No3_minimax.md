# Ex.No: 3  Implementation of Minimax Search
### DATE: 12.08.2023                                                                           
### REGISTER NUMBER : 212221220061
### AIM: 
Write a mini-max search algorithm to find the optimal value of MAX Player from the given graph.
### Algorithm:
1. Start the program
2. import the math package
3. Specify the score value of leaf nodes and find the depth of binary tree from leaf nodes.
4. Define the minimax function
5. If maximum depth is reached then get the score value of leaf node.
6. Max player find the maximum value by calling the minmax function recursively.
7. Min player find the minimum value by calling the minmax function recursively.
8. Call the minimax function  and print the optimum value of Max player.
9. Stop the program. 

### Program:
```
treeDepth = math.log(len(scores), 2)  # calculate depth of node  log 8 (base 2) = 3)
           print("The optimal value is : ", end="")
           print(minimax(0, 0, True, scores, treeDepth))
import math
	def minimax(curDepth, nodeIndex, maxTurn, scores, targetDepth):
    	    # base case : targetDepth reached
    	    if (curDepth == targetDepth):
        	        return scores[nodeIndex]
    	  if (maxTurn):
        	        return max(minimax(curDepth + 1, nodeIndex * 2,False, scores, targetDepth),minimax(curDepth + 1, nodeIndex * 2 + 1,False, scores, targetDepth))
               else:
        	       return min(minimax(curDepth + 1, nodeIndex * 2, True, scores, targetDepth),
                   minimax(curDepth + 1, nodeIndex * 2 + 1,True, scores, targetDepth))

            # Driver code
           scores = [3, 5, 2, 9, 12, 5, 23, 20]
```











### Output:
![image](https://github.com/viswapriyaG/AI_Lab_2023-24/assets/131427787/9f92645a-5f50-493d-a98e-245464ada1d8)




### Result:
Thus the optimum value of max player was found using minimax search.
