#                                                                                CONVEXPANOU
 The purpose of this package is to provide a method called convex_hull_polygon which consists of three main functions (it includes other supportive as well), with input  a set of 2d points .
The three main functions are:

1) A function named convex_hull_from_points  with output the set of 2-d points which form the convex hull polygon enclosing all the points of the original 2-d set provided as input. For example, if datapoints is your set of 2-d points, convexpanou.convex_hull_polygon(datapoints).convex_hull_from_points() returns the set of 2-d points that forms the convex_hull_polygon thath surrounds all the points of the original dataset. The convex_hull is calculated using the graham scan algorithm. It is mandatory to provide a 2-d array consisting of at least one point.

2) A function named point_is_in_polygon with input, a single 2d point  output: True or False, depending on whether the point lies inside / on the convex polygon (true) OR outside the polygon (false) provided originally as the 2-d set input of points in the method. For example, if datapoints is your convex hull polygon and p is your point,, if you want to find out whether p lies inside datapoints, you call convexpanou.convex_hull_polygon(datapoints).point_is_in_polygon(p). Please mind the following: 
     a) When trying to find out whether a 2-d point is into the convex _hull inserted (using the function point_is_in_polygon of convex_hull_graham method), if the point lies in the boundaries of the polygon, it returns False as if the point is NOT into the polygon.                                                                      
     b) The function does not check whether the points provided as a 2-d array convex -hull polygon, actually do form a convex hull polygon. If you are not sure, please implement the function convex_hull_from_points first.                                                                              
     c) It is mandatory to provide as input point in the function point_is_in_polygon an array of (1,2) shape.                                                                                                                                     
 3) A function named do_intersect with input: two convex polygons and output: true or false, depending on whether the two provided polygons intersect. For example, if datapoints is your first convex hull polygon and datapoints2 is your second convex hull polygon and you want to find out whether these two do intersect,  you call pointconvexpanou.convex_hull_polygon(datapoints).do_intersect(datapoints2). Please mind the following:                                
    a) The function does not check whether the points provided as a 2-d array convex -hull polygons, actually do form  convex hull polygons. If you are not sure, please implement the function convex_hull_from_points first in both 2-d sets of points.                                                                                      
    b) If one convex_hull_polygon is completely inside the other one, the function returns True as these two polygons do intersect

 Other supportive functions of the method are: 
    a) plt_graham_convex() which plots the whole set of points and forms the convex_hull_polygon that surrounds them.
    b) plt_in_or_out(p) with input a point p (an array shaped (1,2)), which plots the convex_hull_polygon provided as well as the point p
    c) plt_in_or_out_conv (datapoints2) which plots both convex_hull_polygons provided as input in order to visualize whether they do intersect or not
            
