# Jamie and Ben's coding adventure!

In this repository we're going to code some linear regression, which is essentially finding the ideal line of best fit between chunks of data. To do this we'll use the numpy library, the main idea comes from having $n$ pairs of points of the form $(x_i,y_i)$ where $i$ goes from $1$ to $n$ inclusive, suppose we have some estimate $\hat{y}_i$ that depends on the input $x_i$ then we can write $\hat{y}_i = \hat{y}(x_i)$. (a function of $x_i$).

We now want to draw a line such that $\hat{y}(x_i)$ is as close as possible to $y_i$, so that the estimate is `accurate`, in other words we want to `minimise` the difference between them, i.e $\hat{y}(x_i) - y_i$ for every value of $i$. Generalising this idea we want to minimise the `average` distance between the line and the data, so this looks like:

$$
MSE(\bold{x,y}) =\frac{1}{n} \sum^{n}_{k=1}{(\hat{y}(x_i)-y_i)^2}
$$

We square the difference as we only care about the dfference being as near to zero as possible, think of this as being the distance between the point and the line squared, hence we call this the `mean squared error` (MSE), $\bold{x} = (x_1, \dots,x_n)$ is the vector of input data, and $\bold{y} = (y_1, \dots,y_n)$ is the vector of desired output data!

Boom! We have our problem mathematically formulated, so we want to mninimise the MSE of the data, then we will find our line! Usually (for linear regression i.e straight lines) $\hat{y}(x_i) = mx_i + c$, and this problem involves finding m and c such that MSE is minimised, then we have our equation for y hat!
