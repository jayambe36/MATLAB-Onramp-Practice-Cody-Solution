
# MATLAB Onramp Practice Cody Solution

RANK 5,427 of 108,192
my profile link :- 
https://in.mathworks.com/matlabcentral/profile/authors/20986667?s_tid=gn_comm




## Authors

- [@jayambe36](https://www.github.com/jayambe36)


## SOLUTION CODE LINK

https://github.com/jayambe36/MATLAB-Onramp-Practice-Cody-Solution

## 🚀 About Me
I'm a Passionate DATA SCIENTIST.


## 🔗 Links
[![linkedin](https://img.shields.io/badge/linkedin-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/jayambe/)


## Acknowledgements

 - [Make a Good readme online](https://readme.so/editor)


## Support to improve Matlab by

- MathWorks


## QUESTION : 1

Times 2 - START HERE
Try out this test problem first.
Given the variable x as your input, multiply it by two and put the result in y.
Examples:
Input x = 2
Output y is 4

Input x = 17
Output y is 34

============================================

function y = times2(x)
  y = x*2;
end

============================================





## QUESTION : 2

Calculate Amount of Cake Frosting
Given two input variables r and h, which stand for the radius and height of a cake, calculate the surface area of the cake you need to put frosting on (all around the sides and the top).
Return the result in output variable SA.

============================================

function SA = func_frosting(r,h)
  SA = (pi*r^2)+(2*pi*r*h);
end

============================================





## QUESTION : 3


Convert from Fahrenheit to Celsius
Given an input vector F containing temperature values in Fahrenheit, return an output vector C that contains the values in Celsius using the formula:
C = (F–32) * 5/9

============================================

function C = temp_convert(F)
  C = (F-32)*(5/9)
end

============================================





## QUESTION : 4

Find the Oldest Person in a Room
Given two input vectors:
name – user last names
age – corresponding age of the person
Return the name of the oldest person in the output variable old_name.

============================================

function old_name = find_max_age(name,age)
    old_name=name(find(age==max(age)));
end

============================================





## QUESTION : 5

Verify Law of Large Numbers
If a large number of fair N-sided dice are rolled, the average of the simulated rolls is likely to be close to the mean of 1,2,…N i.e. the expected value of one die. For example, the expected value of a 6-sided die is 3.5.
Given N, simulate 1e8 N-sided dice rolls by creating a vector of 1e8 uniformly distributed random integers. Return the difference between the mean of this vector and the mean of integers from 1 to N.

============================================

function dice_diff = loln(N)  
dice_diff = mean(randi(N, 1e8,1)) - (N+1)/2;
%randi(x,y,z) here x denotes the maximum value. y and z represent the size of the matrix yxz
end

============================================










## QUESTION : 6

Solve a System of Linear Equations
Example:
If a system of linear equations in x₁ and x₂ is:
2x₁ + x₂ = 2
x₁ – 4 x₂ = 3
Then the coefficient matrix (A) is:
2 1
1 -4
And the constant vector (b) is:
2
3
To solve this system, use mldivide ( \ ):
x = A\b
Problem:
Given a constant input angle θ (theta) in radians, create the coefficient matrix (A) and constant vector (b) to solve the given system of linear equations in x₁ and x₂.
cos(θ) x₁ + sin(θ) x₂ = 1
-sin(θ) x₁ + cos(θ) x₂ = 1

============================================

function x = solve_lin(theta)
    A=[cos(theta),sin(theta);-sin(theta),cos(theta)] ; 
    b=[1;1];
    x = A\b; 
end

============================================





## QUESTION : 7

Calculate a Damped Sinusoid
The equation of a damped sinusoid can be written as
y = A.ⅇ^(-λt)*cos(2πft)
where A, λ, and f are scalars and t is a vector.
Calculate the output sinusoid y given the inputs below:
lambda – λ
T – maximum value of t
N – number of elements in t
Assume A = 1 and f = 1 . The vector t should be linearly spaced from 0 to T, with N elements.

============================================

function y = damped_cos(lambda, T, N)
  t=0:T/(N-1):T;
  y = exp(-lambda*t).*cos(2*pi*t);
end

============================================





## QUESTION : 8

Plot Damped Sinusoid
Given two vectors t and y, make a plot containing a blue ( b ) dashed ( — ) line of y versus t.
Mark the minimum value m of the vector y by adding a point to the plot. This point should be a red asterisk marker, and it must be added after the blue line.

![App Screenshot](data:image/png;base64,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)

Return the minimum value of y as output m.

============================================

function m = plot_cos(y, t)
[m,pos] = min(y);
plot(t,y,'b--',t(pos),m,'r*');
end

============================================





## QUESTION : 9

Calculate BMI
Given a matrix hw (height and weight) with two columns, calculate BMI using these formulas:
1 kilogram = 2.2 pounds
1 inch = 2.54 centimeters
BMI = weight(kg) / [height(m)]^2
The first column is the height in inches. The second column is the weight in pounds.

============================================

function bmi = bmi_calculator(hw)  
    hw(:,1)=hw(:,1)*2.54/100;
    hw(:,2)=hw(:,2)/2.2;
    bmi=hw(:,2)./(hw(:,1).^2);
end

============================================





## QUESTION : 10

Crop an Image
A grayscale image is represented as a matrix in MATLAB. Each matrix element represents a pixel in the image. An element value represents the intensity of the pixel at that location.
Create a cropped image matrix Icrop using inputs given in the following order:
I – Grayscale input image
Rmin – Lowest row number to retain
Cmin – Lowest column number to retain
Rpix – Number of pixels along rows to retain
Cpix – Number of pixels along columns to retain

For example, if your image was:
I = [1 2 3 4
5 6 7 8]
And you called crop_image with inputs
Icrop = crop_image(I, 2, 2, 1, 3)
The output Icrop should be
[6 7 8]

============================================

function Icrop = crop_image(I, Rmin, Cmin, Rpix, Cpix)
  Icrop = I(Rmin:Rmin+Rpix-1,Cmin:Cmin+Cpix-1);
end

============================================





## QUESTION : 11

Find the Best Hotel
Given three input variables:
hotels – a list of hotel names
ratings – their ratings in a city
cutoff – the rating at which you would like to cut off
return only the names of those hotels with a rating of cutoff value or above as a column vector of strings good.

============================================

function good = find_good_hotels(hotels,ratings,cutoff)
  good = hotels(find(ratings>=cutoff))
end

============================================





## QUESTION : 12

Find MPG of Lightest Cars
The file cars.mat contains a table named cars with variables Model, MPG, Horsepower, Weight, and Acceleration for several classic cars.
Load the MAT-file. Given an integer N, calculate the output variable mpg.
Output mpg should contain the MPG of the top N lightest cars (by Weight) in a column vector.

============================================

function mpg = sort_cars(N)
    load cars.mat
    sorted = sortrows (cars,4);
    mpg = sorted(1:N,2);
    mpg=mpg{:,:};
end

============================================





## QUESTION : 13

Calculate Inner Product
Given two input matrices, x and y, check if their inner dimensions match.
If they match, create an output variable z which contains the product of x and y
Otherwise, z should contain a custom string message
Example:
x = [1 2;3 4]
y = [5;6]
z = [17;39]
x = [1 2 3;4 5 6]
y = [2 5;3 6]
z = “Have you checked the inner dimensions?”
OR
z = “The inner dimensions are 3 and 2. Matrix multiplication is not possible”

============================================

function z = in_prod(x,y)
    [m,n]=size(x);
    [a,v]=size(y);
    if(n==a)
        z=x*y;
    else
        z="c";
    end
end

============================================





## QUESTION : 14

Rescale Scores
Each column (except last) of matrix X contains students’ scores in a course assignment or a test. The last column has a weighted combination of scores across all the assignments and tests.
Replace the elements in the last column of this matrix with a GPA calculated based on the following scale:
Score GPA
90 – 100 3 – 4
80 – 90 2 – 3
70 – 80 1 – 2
60 – 70 0 – 1
Below 60 0
Assume that no student in this class has scored below 60. Also note that the mapping in the range [60, 100] is linear.

============================================

function X = rescale_scores(X)
    X(:,end)=(X(:,end)-60)/10;
end

============================================





## QUESTION : 15

Longest run of consecutive numbers
Given a vector a, find the number(s) that is/are repeated consecutively most often. For example, if you have
a = [1 2 2 2 1 3 2 1 4 5 1]
The answer would be 2, because it shows up three consecutive times.
If your vector is a row vector, your output should be a row vector. If your input is a column vector, your output should be a column vector. You can assume there are no Inf or NaN in the input. Super (albeit non-scored) bonus points if you get a solution that works with these, though.

============================================

function val=longrun(a)
max_num=0;
val=[];
j=1;
last_item=nan;
item_num=0;
for i=1:length(a)
    if a(i)==last_item
        item_num=item_num+1;
        if item_num==max_num
            j=j+1;
            val(j)=a(i);
            
        elseif item_num>max_num
            max_num=item_num;
            j=1;
            val=[];
            val(j)=a(i);
        end
    
    else
        if max_num<=1
            max_num=1;
            val(j)=a(i); 
            j=j+1;
        end
        last_item=a(i);
        item_num=1;
    end
end
[m,n]=size(a);
if m>1
    val=val';
end
end

============================================

