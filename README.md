# Denavit-Hartenberg-matrix-library
A library to easily operate DH matrixes and compute forward kinematics



Example:

//INIT

Mat4 T1(alpha1, a1, d1); 
Mat4 T2(alpha2, a2, d2); 
Mat4 T3(alpha3, a3, d3); 
Mat4 T4(alpha4, a4, d4); 

Mat4 T14; 

//IN MAIN LOOP

T1.update(theta1); 
T2.update(theta2); 
T3.update(theta3); 
T4.update(theta4); 

T14.write(T4); 
T14.multiply(T3); 
T14.multiply(T2); 
T14.multiply(T1); 
 
// NOW T14 IS THE DIRECT TRANSFORM MATRIX

T14.verbose();
