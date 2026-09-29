# AutoRev1

## Approach and Solution
Connected to the instance provided. A huge binary text was printed out and we have to find the secret number within that huge text which was printed within 1 second only. 
Asked Gemini, how to write a python code, to find the secret, enter it , then loop the code again to do this 20 times. 

![alt text](image.png)
Explainin the code:
![alt text](image-1.png)
1. Import pwn tools, allows python to use powerful pwn tools to solve CTF questions which is not possible with python's default library. 
2. HOST, PORT contain the host link and port to connect to the instance. 
3. r.remote uses the HOST, PORT data to create a remote connection to the instacnce.
4. for loop is used here to the loop the code written in the loop to loop 20 times because there are 20 binaries. 
5. r.recvuntil() reads all the text data sent by the server and waits.
6. r.recvline()Reads the line sent by the server which contains all the binary in hex form. .strip() removes all extra whitespaces and removes all extra uncessary new lines, etc .
7. hex_blob.decode() Converts all the bytes sent by the server in hex. 
8. bytes.fromhex() converts the hex back into data which the machine can read. 
9. \xc7\x45\xfc this is common sequence which the compiler creates and this was discovered by rev engineers after anaylising many codes.
10. binary.find() Finds the exact starting point of \xc7\x45\xfc this in the converted hex to bytes. 
11. if not found, it would print Not found.
12. binary[idx+3:idx +7] --> slicing the array to get the 4bytes needed.
13. u32 converts those 4 bytes into correct mathematical order. Then converts thoes hex bytes into human readable numbers.
14. log.sucess --> this sends the extracted secret to the terminal
15. r.recvuntil(b"What's the secret") --> Waits till the server prints What's the secret
16. r.sendline() --> sends the secret extracted back to the server.
17. print(r.recvall().decode()) --> this line waits till the server sends the remaining text data, after all the 20 binaries are done , to get the glag. 

18. Source: Gemini, Infosec

## Flag
academy{4u7o_r3v_g0_brrr_78c345aa}