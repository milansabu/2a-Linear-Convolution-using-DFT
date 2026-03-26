## EXPT 2a: LINEAR CONVOLUTION-USING-DFT
## AIM
To perform and verify linear convolution operation of two given sequences using SCILAB.

## APPARATUS REQUIRED
PC installed with SCILAB

## PROGRAM:
LINEAR CONVOLUTION
```
clc;
clear;
x = [1 1 1 1];
h = [1 2 3 4];
m = length(x);
n = length(h);
a = 0:1:m-1;
b = 0:1:n-1;
subplot(3,1,1);
plot2d3(a,x);
xlabel('Time');
ylabel('Amplitude');
title('Graphical Representation of Input Signal X');
subplot(3,1,2);
plot2d3(b,h);
xlabel('Time');
ylabel('Amplitude');
title('Graphical Representation of Impulse Signal h');
for i = 1:n+m-1
    conv_sum = 0;
    for j = 1:i
        if (((i-j+1) <= n) & (j <= m)) then
            conv_sum = conv_sum + x(j)*h(i-j+1);
        end
    end
    y(i) = conv_sum;
end
disp(y,'Convolution Sum using Direct Formula Method = ')
subplot(3,1,3);
plot2d3(y)
title('Graphical Representation of output Signal y');
```





### CALCULATIONS:

![WhatsApp Image 2026-03-27 at 4 44 50 AM](https://github.com/user-attachments/assets/0a1d9e41-ba7e-4be7-89f1-0cb66472f8ad)

![WhatsApp Image 2026-03-27 at 4 44 49 AM (1)](https://github.com/user-attachments/assets/9b0b1ee9-7baf-4fab-acf0-3093f1566b1d)


### SAMPLE OUTPUT:

<img width="752" height="698" alt="image" src="https://github.com/user-attachments/assets/fa12c742-4afb-40b0-8c85-977c88fc53ad" />




RESULT:
Thus, the linear convolution of the two given sequences were performed and its result was verified.
