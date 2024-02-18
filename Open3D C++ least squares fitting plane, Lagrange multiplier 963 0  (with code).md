##  First, the principle of the algorithm 

  Let the fitted plane equation be: Constraint conditions are: plane parameters can be obtained. At this time, to make the obtained fitted plane is optimal, that is, to minimize the sum of squares of the distance from the point to the plane, that is, to satisfy: In the formula,, is the distance from any point in the point cloud data to this plane. To make, you can use the Lagrange multiplier method to solve the extreme value and get the function:  

  First, find the partial derivative on both sides of formula (2-4), and let the partial derivative be zero, to obtain: let,,, the center of mass be,,, then: then find the partial derivative on both sides of formula (2-4), get  

  The above equations form the eigenvalue equation: In the equation, then, to solve the plane parameters is to solve the eigenvalues and eigenvectors of the matrix. And because it is a third-order real symmetric matrix, the eigenvalue solution formula is: under constraints, get. Therefore, the minimum value is the minimum eigenvalue of the matrix, and the corresponding eigenvector is a plane parameter, which can be obtained by using the centroid. 

##  Code implementation 

 ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574534277
 ```  
##  III. Display of results 

 ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574534277
 ```  
