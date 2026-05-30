# Simulation of Mean and Variance using SCILAB
### Aim:
To write a program for mean, variance and cross correlation in SCILAB and verify the output.

### Equiptments Required:
• Computer

• SCI LAB

### Algorithm:
1. Define the Function: Specify the function you want to simulate. For example, f(x)=sin⁡(x)f(x) = \sin(x)f(x)=sin(x) or any other function.
2. Generate Sample Points: Decide on the range and the number of sample points. Generate these sample points within the desired range.
3. Evaluate the Function: Compute the function values at each of these sample points.
4. Compute Mean, Variance and Cross Correlation: Use Scilab's functions to calculate the mean and variance of the computed function values.
5. Display Results: Output the computed mean variance and Cross Correlation.
   
### Procedure:
  • Refer Algorithms and write code for the experiment.

  • Open SCILAB in System.
  
  • Type your code in New Editor.
  
  • Save the file.
  
  • Execute the code.
  
  • If any Error, correct it in code and execute again.
  
  • Verify the generated results.
  
### Program:
~~~
clear;
clc;
function z=f(x)
    z=x.*4.*(1-2.*x).^2;
endfunction
a=0;
b=1;
EX=intg(a,b,f);
function z=c(y)
    z=y.*4.*(1-2.*y).^2;
endfunction
EY=intg(a,b,c);
disp(EX,"i)Mean of X =")
disp(EY,"Mean of Y =")
function z=g(x)
    z=x.^2.*4.*(1-2.*x).^2;
endfunction
EX2=intg(a,b,g);
function z=h(y)
    z=y.^2.*4.*(1-2.*y).^2;
endfunction
EY2=intg(a,b,h);
vX2=EX2-(EX)^2;
vY2=EY2-(EY)^2;
disp(vX2,"ii)Variance of X =")
disp(vY2,"Variance of Y =")
x=input("type in the reference sequence=");
y=input("type in the second sequence=");
n1=max(size(y))-1;
r=corr(x,y,n1);
plot2d3(r);
xtitle("Cross Correlation");
~~~

### Calculation:

### Output:

<img width="522" height="503" alt="Screenshot 2026-05-21 134911" src="https://github.com/user-attachments/assets/cb343c4c-8a97-48c7-8ade-33a755198e96" />

<img width="762" height="693" alt="Screenshot 2026-05-21 134606" src="https://github.com/user-attachments/assets/cae45466-4d1f-40a4-97ae-6886e2408ad6" />

### Result:
Thus the mean , variance and cross correlation are executed in Scilab and output is verified.
