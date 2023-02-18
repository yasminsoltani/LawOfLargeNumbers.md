# Law of Large Numbers 🎰 🂡 

### What is the law of large numbers? 

In Mathematics is defined as 

<img width="381" alt="Screenshot 2023-02-18 at 2 27 39 PM" src="https://user-images.githubusercontent.com/103854541/219895228-a99bcb00-5da1-4425-8ce2-b0ec3199ad13.png">

<img width="433" alt="Screenshot 2023-02-18 at 2 29 09 PM" src="https://user-images.githubusercontent.com/103854541/219895505-237d8386-9b45-4ab6-999d-ae34f7decf99.png">


In probability and statistics, the law of large numbers says that as a sample size increases (Xn), its mean gets closer to the average of the entire population (Ex). This is because as the sample size increases, the sample becomes more representative of the population.

Let's assume that we flip a coin 10, 100, 1000, times and count how many times we get heads or tails. Intuitively speaking, we should expect to have 50% chance of getting heads and 50% of getting tails.

| NumOfTimes | Heads | Tails | Percentage of Heads | Percentage of Tails |
| ---------- | ----- | ----- | ------------------- | ------------------- |
| 10 | 3 | 7 | 30% | 70% |
| 100 | 47 | 53 | 44% | 56% |  
| 1000 | 502 | 498 | 50.2% | 49.8% |
  
 We can see, that if we flip the coin 10 times, the percentages are too off from being 50% each; however, as we increase the number of times the coin is flipped, average rates approach the expected value.

### Ever wondered why gamblers always end up loosing? Why do they have a much lower chance of winning than losing?

<img src="https://user-images.githubusercontent.com/103854541/219891093-380b2c22-0585-44f8-9641-7f9e8d5c4185.png" width="400" height="300"> [[1]](https://www.10best.com/interests/hotels-resorts/casino-rankings-top-10-not-las-vegas/)

Every day, casinos and other gambling businesses operate on the principle of the Law Of Large Numbers. In the short term, people might beat the house, but over the long-term the house will always prevail because of the criterion of the games they make you play. 


## 📌  R Exercise  
Courtesy of Kirill Emerenko

Test the Law Of Large Numbers for N random normally distributed numbers with mean = 0, stdev = 1 (stdv = standard deviation):

Create an R script that will count how many of these numbers fall between -1 and 1 and divide by the total quantity of N

You know that E(X) = 68.2%

Check that Mean (Xn) -> E(X) as you rerun your script while increasing N 

```R
N <- 100 #specify sample size
counter <- 0 #reset counter
for(i in rnorm(N)){ #iterate over vector of numbers
  if(i>-1 & i<1){ #check where iterated variable falls
  counter <- counter +1 #increase counter if condition is met
  }
 }
answer <- counter/ N  #calculate hit ratio
answer  #print answer in console

```

#### Result

![1](https://user-images.githubusercontent.com/103854541/219899291-21b7e29b-3491-41f3-a77f-8229593c7fc8.jpg)

Because we want E(X) to get closer to 68.2%, we try increase N to 1000

```R
N <- 1000 #specify sample size
counter <- 0 #reset counter
for(i in rnorm(N)){ #iterate over vector of numbers
  if(i>-1 & i<1){ #check where iterated variable falls
  counter <- counter +1 #increase counter if condition is met
  }
 }
answer <- counter/ N  #calculate hit ratio
answer  #print answer in console

```

#### Result


![3](https://user-images.githubusercontent.com/103854541/219899346-584889e5-dd27-4d99-b82e-a2b723d21c53.jpg)

And now increase it to 10,000

```R
N <- 10000 #specify sample size
counter <- 0 #reset counter
for(i in rnorm(N)){ #iterate over vector of numbers
  if(i>-1 & i<1){ #check where iterated variable falls
  counter <- counter +1 #increase counter if condition is met
  }
 }
answer <- counter/ N  #calculate hit ratio
answer  #print answer in console

```

#### Result

![4](https://user-images.githubusercontent.com/103854541/219899377-e7cd9b66-b91a-41ac-8b7a-453ca7e9389f.jpg)

As we can see, the more times we iterate, the closer we get to E(X)= 68.2%


Absolutely loved this exercise, the link to the R course [here](https://www.udemy.com/course/r-programming/)
