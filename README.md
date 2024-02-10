# CGI_Assignment1

### Adjustments for m>1:
In the original Bresenham's Line Drawing Algorithm, the decision parameter calculation and pixel selection are based on the change in the x-coordinate.
However, when m>1, the algorithm needs to consider the change in the y-coordinate instead of the x-coordinate.The modification is needed because the line is steeper in the vertical direction than in the horizontal direction.
The modification involves :
+ **Swapping Coordinates:** The X and Y coordinates of the input points are swapped.
+ **Decision Parameter Modification:** The base case for decision parameter (d) is adjusted to d_new = 2 * dx - dy  and for general case, decision parameter (d) is adjusted to
+ if d_previous<0 then,d_next = d_previous + 2 * dx
+ if d_previous>=0 then, d_next= d_previous +2 * dx - 2 * dy

### For Case 1: (1,1),(8,4)
+ *Slope :* m=(4-1)/(8-1)=3/7<1
+ *Intermediate Coordinates:* {(1, 1), (2, 1), (3, 2), (4, 2), (5, 3), (6, 3), (7, 4), (8, 4)}
+ *Decision Variables:*  {-1, 5, -3, 3, -5, 1, -7, -1}
![Screenshot (1)](https://github.com/Bulbul80SWE/CGI_Assignment1/assets/103897359/88005112-28f2-4d73-b5d6-9ca5b4205c3a)


### For Case 2: (1,1),(4,8)
+  *Slope :* m=(8-1)/(4-1)=7/3>1
+ *Intermediate Coordinates:* {(1, 1), (1, 2), (2, 3), (2, 4), (3, 5), (3, 6), (4, 7), (4, 8)}
+ *Decision Variables:*  {-1, 5, -3, 3, -5, 1, -7, -1}
![Screenshot (2)](https://github.com/Bulbul80SWE/CGI_Assignment1/assets/103897359/026969ad-ac13-402e-8894-c6ab63c23835)
