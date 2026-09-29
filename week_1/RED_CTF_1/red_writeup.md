# RED

## Approach and Solution
I started by first downloading the PNG file. I used exiftool on it(very common ). Then I saw there was some poem in that. Then I copied that poem into a notepad so that i could see it clearly.
Then I started trying to decode the poem. Then I so that there were different orders of 'dots'('.'). I thought that was morse code, but I was wrong. Then I was stuck. But then I realised there is type of poem in which there is word and using each letters of the poem we write a poem. Then I took all the first letters of each line and wrote it came as 'CHECKLSB'. I didnt know what is check LSB. Then, I went on google to search what is CHECKLSB. But unfortunatelty, google showed me that this was part of picoCTF "RED" Foresenic challenge. But I still did the CTF, how I was meant to do. Then, I checked on google how to check for LSB in a picture. I had install some tool called "zsteg", I installed it. Then I ran the command. It showed a text which looked like base64 encoded. Then a decoded it and it gave me the flag.

## Screenshots
![exiftool used](image-1.png)
![acrostic poem](image-2.png)
![CHECKLSB](image-3.png)
![What is LSB](image-4.png)
![Installing zsteg](image-5.png)
![zsteg used](image-6.png)
![Base64 encoded](image-7.png)
![Base64 decode flag obtained](image-8.png)

## Flag
picoCTF{r3d_1s_th3_ult1m4t3_cur3_f0r_54dn355_}

## Takeaway
I will remember what is LSB(Least Significant Binary), try to look at data better and try to understand clues. I will use zsteg tool. 