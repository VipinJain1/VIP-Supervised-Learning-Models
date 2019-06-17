### Note:
Any help needed to execute the code or understanding the code, please send me message. I will soon upload the input data and expected output data.
More updates coming soon. Meanwhile Please look at the code. I have added some comments over there.  

# Supervised-Learning-Models

### SVM: Popular and simple algorithm.

#### Geometric Intution:

Separate positive points from negative points by drawing multiple planes. We want a plane that separates my positive 
points from negative points as widely as possible from all other planes. That plane is called margin maximizing hyper plane.
SVM tries to find hyper plane that maximizes the margin between positive and negative points. As margin increases, my generalization accuracy improves.

#### Support Vector:

Points that on positive hyper plane and points that are on negative hyper plane are called support vectors. 
So my actual plane will be between positive plane and negative plane.

#### Convex Hull:

I have bunch of points,  I can draw a polygon such that all the points either inside polygon or on the edges of polygon.If points are inside polygon or on the polygon, I need to go through those points of polygon, which are inside of polygon, so it is convex.
So points to summarize as below:

(1) Convex hull of +ve points  and -ve points.
(2) Find the shortest line connnecting these hulls since I have drawn many hulls.
(3) Bisect the line.  - divide the line into two equal parts. So that line is margin maximing plane that has maximum distance.

### Mathamatical Forumlation of SVM:

$ = margin-maximizing 
$  : W(t)x+b =0 # plance equation, (t)transpose is used since we need to measure aganist x-axis. 
Transpose you will see everywhere since point is right 90 degree on the axis. b is used since plane is not intersecting origin.

$+ : W(t) x + b =1  # for positive plane.
$- : w(t)x + b = -1  # for negative plane.

in SVN, we just care about margin. Get the distance between plane $+ and $-, so Margin value = 2/||W||

Try to make sure all the +ve points are above $+ plane and all -ve points are below $- plane. That will be a perfect case. This is called "Hard Margin SVM".

Create a new variable - @i such that

@i =0 if Yi * (W(t) Xi + b) >=1 this is correctly classfied $+ (positive plane) and $- ( negative plane).
if @i>0 and equal to some units of distance away from correct hyperplane either of +ve plane or -ve plane in either direction.

We want to minimize errrors or mis classification.  For incorreclty classified points my @i >0.

(W*,B*) = ArgMin(W to B) ||W|| /2 + C 1/n Sum(@i) , last C part is the loss. Total deviation from good points.  C is the hyper 
parameter. 

If I increases, that means tendency to make mistakes reduces so I  tend to overfit my plane. 
If C decreases, I have underfit model and this is called "Soft margin SVM". "Soft margin SVM" means,  we allow errors but try to reduce overall errors.

In hard margin SVM, overfit model, no errors are allowed.

Question:  why +1 and -1 only on hyper plane??

We are saying 'W' could be any vector, not just unit vector.

Margin = 2/||W||, whole task is to maximize margin. 

### Loss-Minimization - Hinge Loss:

Logistic loss to minimize.
Change Logistic to linear loss + regularization ==> Linear regression
SVM ==> Hinge loss + regularization.

### Dual Form of SVM:
ToDo: Remember soft margin SVM and hard margin SVM.
We learnt primal SVM problem earlier.  Primal problem is equal to dual SVM problem.  Formula hard to write here. 

### Kernalization:










 









