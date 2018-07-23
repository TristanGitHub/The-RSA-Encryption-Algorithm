# The RSA Encryption Algorithm

RSA (Rivest–Shamir–Adleman) is a public-key crypto algorithm and used for securely transmit messages. This RSA algorithm uses a encrypted key that is public and it is different from the decryption key which is kept secret. These two keys together are able to decrypt a message. This article will explain more about the RSA encryption Algorithm. 

#### Step 1 You have to pick two prime numbers.

The prime number that are going to be picked have to be enormous like hundreds and hundreds of digits long. If the prime number are to small it will not work. So in this example were going to pick two small primes to show why it will not work and to make it easy to understand. In this example we pick the primes 2 and 7.

**Picked prime numbers:**

p = 2, q = 7

#### Step 2 Come up with a number which is the product of the two primes.

The product number is called N and is in this case 14.  So the primes get multiplied. This number get becomes the modulus in the decryption key en encryption key. So the N gets prophesied but the primes are not.

**The Modulus:**

p * q = 14

N = 14

#### Step 3 The Phi function.

The totient function phi(n), also called Euler's totient function, is defined as the number of positive integers <=n that are relatively prime to (do not contain any factor in common with) n, where 1 is counted as being relatively prime to all numbers. So let's list out all the numbers

1,2,3,4,5,6,7,8,9,10,11,12,13,14

In this list some of these numbers that have common factors with 14 and some have not. So let's cross out the numbers that share a common factor with 14.

1,3,5,9,11,13

So there are 6 number left. These numbers called co prime, because they share no common factors with 14. But what if we had a higher number? So there is a way to calculate this on an easy way.

**Phi function:**

Φ(n) = (p-1)(q-1)

Φ(n) = (2-1)(7-1) = 6

#### Step 4 Encryption key

In the fourth step the code in going to be encrypted. To do that it has to fit certain properties. These number can't be picked randomly. So e (encryption) has to obey two properties.

**Two properties for encryption:**

1. To encrypt the number it has to be between 1 and Φ(n)
2. The second property is that the number has to be co prime with n and Φ(n)

In this case 2,3,4,5 and we can cross out the even numbers. So the numbers 3 and 5 are over. But we can also cross out 3 because it got a common factor with 6. The remaining number is 5.

e = 5 

lock : (5,14)

#### Step 5 Decryption key 

To decrypt the encryption goes as follow. The decryption key times encrypted key (mod  Φ(n)) = 1.

**Decryption goes like this:**

d*e(mod  Φ(n)) = 1 

Earlier the phi function calculated the mod = 6. What is mod 6 of each of these numbers? As you see each 6th multiple is a multiple of 6. This pattern is going to repeat. So any number can be picked where it gets a one. So let's pick 11 as decryption key. 

**The pattern:**

5,10,15,20,25,30, 35,40,45,50,55,60

5,4,3,2,1,0 5,4,3,2,1

**Decryption:**

5 * 11 (mod 6) = 1

So now we have the key (11,14)

