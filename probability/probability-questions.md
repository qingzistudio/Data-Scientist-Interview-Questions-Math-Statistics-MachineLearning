# Probability Questions

 **1.Suppose you toss a fair coin 400 times. What is the probability that you get at least 220 heads? Round your answer to the nearest percent. \(Similar questions: Toss a coin 1000 times, with 400 heads, is a fair coin or not\)**  

This is a central limit theorem questions. The expected value of a fair coin is 1/2 and variance is 1/4. Calculate Z score using algorithms $$Z =(x_i-\bar x)/s $$, then$$Z = (220-200)/(\sqrt{400*1/4})=2$$, the probability that get at least 220 heads is 1-97.5%=2.5%, round the value to 2%. In the similar questions, using Z score of average number $$Z=(x_i-\mu)/(\sigma) = (400-500)/\sqrt{1000/4}=6.32$$, it is an extreme case for a fair coin, so the coin is biased. 

**2. Two basketball teams, A and B, compete in seven games, winner is who wins 4 games first. The probability of A winning each game is 0.5, what is the probability that they have to play all 7 games to decide the winner?**

The event that A and B win 3 times respectively in 6 rounds equals to the event that plays all 7 rounds to decide the winner. P\(A and B win 3 times in 6 rounds\) = $$\frac{C_3^6}{2^6}=\frac{5}{16}$$ 

**3. A and B play a game of tossing a coin one by one. The coin is fair, H for Head and T for Tail. If HTH comes first, then A wins, or HHT comes first, B wins. What is the probability that B wins?**

Suppose P\(B wins\) is P  
if 1st round gets T, then B still wins the game has the probability p/2  
if 1st round gets H, 2nd round get H, then B definitely win the game, which means P\(HHT\|HH\) = 1, then P\(HHT\|HH\)\*P\(HH\) = 1/4  
if 1st round get H, 2nd round get T, 3rd round get H, then A definitely win the game  
if 1st round get H, 2nd round get T, 3rd round get T, then P\(HHT\|HTT\)\*P\(HTT\)=P\(HHT\)/8  
so p = p/2+1/4+p/8, p = 2/3

**4. If we toss a fair coin until two heads continuously, what the average number of trials of tossing**

a. If the first flip is a tails, then we have wasted one flip. The probability of this event is 1/2 and the total number of flips required is x+1   
b. If the first flip is a heads and second flip is a tails, then we have wasted two flips. The probability of this event is 1/4 and the total number of flips required is x+2   
c. If the first flip is a heads and second flip is also heads, then we are done. The probability of this event is 1/4 and the total number of flips required is 2.  
Adding, the equation that we get is x = \(1/2\)\(x+1\) + \(1/4\)\(x+2\) + \(1/4\)2  
Solving, we get x = 6.

**5. How to generate a random number between 1-7 with only a die \[from 120 Data Scientist Interview Questions\]**

Method 1: 1-7 can be represented by 3-bit binary number, for example 1 is 000 and 7 is 111. For each trial a die can toss 3 times, if number smaller than 4, which represents 0, on the other hand it is 1. For example, a trial is \(3,4,5\),  its binary number is \(0, 1, 1\), which is 3  
Method 2: toss a die twice to create a vector \(first number, second number\), the combinations range from \(1, 1\) till \(6,5\) that can be divided into 7 parts of 5 each

**6. How can you get a fair coin toss if someone hands you a coin that is weighted to come up heads more often than tails?  \[from 120 Data Scientist Interview Questions\]**

Yes, if you toss a biased coin twice, the results would be HH, HT, TH, TT, and P\(HT\) = P\(TH\) no mater the coin is biased or not. Then you can make HT as H and TH as T to get a fair coin toss.

**7. Bobo the amoeba has a 25%, 25%, and 50% chance of producing 0, 1, or 2 offspring, respectively. Each of Bobo’s descendants also have the same probabilities. What is the probability that Bobo’s lineage dies out?**























