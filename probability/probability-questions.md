# Probability Questions

 **1. Suppose you toss a fair coin 400 times. What is the probability that you get at least 220 heads? Round your answer to the nearest percent. \(Similar questions: Toss a coin 1000 times, with 400 heads, is a fair coin or not\)**  

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

**7. Bobo the amoeba has a 25%, 25%, and 50% chance of producing 0, 1, or 2 offspring, respectively. Each of Bobo’s descendants also have the same probabilities. What is the probability that Bobo’s lineage dies out? \[from 120 Data Scientist Interview Questions\]**

the probability that Bobo's lineage dies out equals to find the probability that Bob produce 0 offspring. let A as a event of offspring amount, then P\(A = 0\) = P\(A = 0\| A=0\)\*P\(A=0\) + P\(A=0\|A=1\)P\(A=1\) + P\(A=0\|A=2\)P\(A=2\) = 1/4+p/4 + 1/2\*p^2, then p=1/2 

**8. Given draws from a normal distribution with known parameters, how can you simulate draws from a uniform distribution? \[from 120 Data Scientist Interview Questions\]**

Use the technique called the probability integral transform\(universality of the uniform\), which plugs your draw into the CDF of the normal distribution with those parameters. universality of the uniform is   
1\) when you plug a random variable into its own CDF to get uniform distribution, F\(X\) ~ U   
2\) when plug a uniform into the inverse CDF of X, you get a random variable distributed like X

**9. A certain couple tells you that they have two children, at least one of which is a girl. What is the probability that they have two girls?**

$$P(1st=Girl\cap2nd=Girl|\text{At least one is girl}) = \frac{P(1st=Girl\cap2nd=Girl\cap\text{At least one is girl}) }{P(At least one is girl)}=\frac{1/4}{3/4}=1/3$$ 

**10. You have a group of couples that decide to have children until they have their first girl, after which they stop having children. What is the expected gender ratio of the children that are born? What is the expected number of children each couple will have?**

Let X as an event of number of children each couple will have, Y as the sex of a children. then $$E(X) = 1*P(Y=Girl) + 2 *(Y=Boy\cap Y=Girl)+3*P(Y=Boy\cap Y=Boy \cap Y=Girl)+... =1*1/2+2*1/4+3*1/8+... =(1/2+1/4+1/8+...)+1/2*(1/2+2/4+4/16)=1+E(X)/2=>E(X)= 1/2$$ 

**11. How many ways can you split 12 people into 3 teams of 4?**

P\(X\) = 12!/\(4!\*4!\*4!\)/3! =5775, divide by 3! because 3 teams are indistinguishable  

**12. Your hash function assigns each object to a number between 1:10, each with equal probability. With 10 objects, what is the probability of a hash collision? What is the expected number of hash collisions? What is the expected number of hashes that are unused.**

Let A be the event of at least on hash collision, then $$P(A) = 1-P(A^c)=1-\frac{10!}{10^{10}}\approx0.9996$$   
Let H be the number of hash collision, N is the used number, then H = 10-N then $$E(N) = 10*(1-(1-1/10)^{10})\approx6.5132$$, the expected number of collision is E\(H\) = 10-E\(N\)

**13. You call 2 UberX’s and 3 Lyfts. If the time that each takes to reach you is IID, what is the probability that all the Lyfts arrive first? What is the probability that all the UberX’s arrive first?**

 All Lyft come first$$P(1st=Lyft\cap 2st=Lyft\cap 3rd=Lyft)=3/5*2/4*1/3=1/10$$  
All Uber come first  
$$P(1st=Uber\cap 2st=Uber)=2/5*1/4=1/10$$ 

**12. I write a program should print out all the numbers from 1 to 300, but prints out Fizz instead if the number is divisible by 3, Buzz instead if the number is divisible by 5, and FizzBuzz if the number is divisible by 3 and 5. What is the total number of numbers that is either Fizzed, Buzzed, or FizzBuzzed?**

Count\(Fizzed\) = 300/3 = 100, Count\(Buzzed\) = 300/5 = 60, Count\(FizzBuzzed\) = 300/\(3\*5\)=20  
Count\(Fizz or Buzzed or FizzBuzzed\) = Count\(Fizzed\) + Count\(Buzzed\) - Count\(FizzBuzzed\) = 100+60-20=140

**13. On a dating site, users can select 5 out of 24 adjectives to describe themselves. A match is declared between two users if they match on at least 4 adjectives. If Alice and Bob randomly pick adjectives, what is the probability that they form a match?**



**14. A lazy high school senior types up application and envelopes to n different colleges, but puts the applications randomly into the envelopes. What is the expected number of applications that went to the right college?**



**15. Let’s say you have a very tall father. On average, what would you expect the height of his son to be? Taller, equal, or shorter? What if you had a very short father?**





**16. What’s the expected number of coin flips until you get two heads in a row? What’s the expected number of coin flips until you get two tails in a row?**





**17. Let’s say we play a game where I keep flipping a coin until I get heads. If the first time I get heads is on the nth coin, then I pay you 2n-1 dollars. How much would you pay me to play this game?**

  




**18. You have two coins, one of which is fair and comes up heads with a probability 1/2, and the other which is biased and comes up heads with probability 3/4. You randomly pick coin and flip it twice, and get heads both times. What is the probability that you picked the fair coin?**





**19. You have a 0.1% chance of picking up a coin with both heads, and a 99.9% chance that you pick up a fair coin. You flip your coin and it comes up heads 10 times. What’s the chance that you picked up the fair coin, given the information that you observed?**



**What is the probability that a deck of 52 cards, divided into 6 draws with 9 cards each, will have two jokers in the same draw?**

Method-1: the combination two jokers in any draws is  $$C_{4}^{52}=54\times53/2$$ , then the combination two jokers in the same draw is $$6\times C_2^9 = 9\times8\times3$$,  the probability is $$\frac{9\times8\times3}{27\times53}=8/53$$  
Method-2:  the first Joker in the draw 1 is 9/54, the second joker in the draw 1 is $$P(\text{second joker in the draw 1|first joker in the draw 1}) = 8/53$$ , the probability of 2 jokers in the same draw is $$P(\text{first joker in the draw 1})*P(\text{second joker in the draw 1|first joker in the draw 1})*6=(6*9*8)/(53*53)=8/53$$ 

  


