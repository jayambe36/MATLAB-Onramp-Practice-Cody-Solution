
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

