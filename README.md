# Supervised-Learning-Models

### SVM: Popular and simple algorithm.

#### Geometric Intution:

Separate positive points from negative points by drawing multiple planes. We want a plane that separates my positive 
points from negative points as widely as possible from all other planes. That plane is called margin maximizing hyper plane.
SVM tries to find hyper plane that maximize the margin between positive and negative points. as margin increases, my generalization accuracy improves.

#### Support Vector:

Points that on positive hyper plane and points that are on negative hyper plane are called support vectors. 
So my actual plane will be between positive plane and negative plane.

Convex Hull:

I have bunch of points,  I can draw a polygon such that all the points either inside polyson or on the edges of polygon.If points are in polygon or on the polygon, I need to go through those points  of polygon which are inside of polygon, so it is convex.
so:
(1) Convex hull of +ve points  and -ve points.
(2) Find the shortest line connnecting these hulls since I have drawn many hulls.
(3) Bisect the line.  - divide the line into two equal parts. So that line is margin maximing plane that has maximum distance.

### Mathamatical Forumlation of SVM:

$ = margin-maximizing 
$  : W(t)x+b =0
$+ : W(t) x + b =1
$- : w(t)x + b = -1
in SVN, we just care about margin. Get the distance between plane $+ and $-, so Margin value = 2/||W||

Try to make sure all the +ve points are above $+ plane and all -ve points are below $- plane. That will be a perfect case. This is called hard margin SVM.

Create a new var, @i such that
@i =0 @i =0 if Yi ( W(t) Xi + b) >=1 this is correctly classfied $+ and $-.
if @i>0 and equal to some units of distance away from correct hyperplane either of +ve plane or -ve plane in either direction.





 









