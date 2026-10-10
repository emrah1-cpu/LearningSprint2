# Learning Sprint #2 — Problem 1 Reflection

**Group:** HackerTeam # 22 
**Contributors:** Emrah Sadikov

## What I learned

-For the learning sprint, I made an application that shows how integer overflow works. This project increased my understanding on how integers use a limited number of bits and what happens when arithmetic overflow occurs.
-An example in the application is adding 120 and 20 using signed 8-bit integers. The result is 140, but the stored result is -116 because the 8 bit signed range is from -128 to 127
-The application also shows the difference between signed and unsigned integers. Using the signed/unsigned option allows to compare how the same bits can represent different values

## My development workflow

-I used ChatGPT to help develop the application using HTML, CSS, and JavaScript. AI was used to assist in generating initial code, organize the interface, provide example calculations, and create test cases
- The application was designed to run in a browser without any additional software. After generating the project files, I organized them and uploaded them to GitHub
- The project also contains a test.js file with test cases showing different integer widths, overflow conditions, and invalid inputs

## What I would improve

- One improvement I would make is adding an animation that shows how carry bits move during adding binary values. I feel like this could help users understand how an arithmetic operation produces an overflow better. 
