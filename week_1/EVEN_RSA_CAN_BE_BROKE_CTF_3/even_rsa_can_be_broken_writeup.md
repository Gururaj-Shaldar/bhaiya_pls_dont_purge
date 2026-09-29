# EVEN RSA CAN BE BROKEN

## Approach
First, I excuted the connection command given. It gave N, e and cypher text. Using that I started to calculate to find the flag. 


## Solution
1. Connect using netcat. Using the command given.
2. N, e and cypher text given. 
3. N = p x q (p and q are 2 prime numbers). 
4. Then I searched for tools which do this for me, then AI told me that the numbers are so big that it is difficult to find p and q. It said I can try to find the prime number myself. 
5. I saw the N was even so it can be divided by 2, which is prime number. So, i told AI to divided my N by 2 (I am not dividing that big number). It gave N/2. 
6. So my p and q are 2 and N/2.
7. Now we have to calulate phi(N). phi(N) = (p-1) x (q-1)
8. phi(N) = (1) x ((N/2) - 1)
9. Now we can use (d x e) x (mod(phi(N))) = 1 
10. I found d.
11. Now we find the message(m): m = c^d (mod N)
12. c is the cypher text
13. Again told AI to find m. Which is a very large number. 
14. Again told AI, to decrypt it and give the hidden message. 


## Takeaway
I learned how RSA works, and how to find the hidden message, if some critical values are given. Like in this case N,e and cypher texr. 

## Flag
picoCTF{tw0_1$_pr!m3de643ad5}