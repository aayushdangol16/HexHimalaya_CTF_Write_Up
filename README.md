# HexHimalaya_CTF_Write_Up
# Getting Started
## Learn to submit flag
### Description:
Flags are case sensitive and all flags should be wrapped in CTF{<answer>}.

Type CTF{THIS_IS_A_FLAG} in the box below.
#### Solution
In description there is a flag



# OSINT
## Mysterious IP
### Description:
157.240.241.35
What is the ASN number and isp of the ip address?

Flag format: CTF{ASNnumber_ISP}
#### Solution
Searching ASN and ISP of 157.240.241.35 on https://hackertarget.com/as-ip-lookup/ 

## Pincode
### Description:
During our surveillance of Phein's networks, our recon team successfully acquired intel indicating the enemy's diminished strength. Consequently, they sought aid from Hexagon and shared the coordinates of their hidden stronghold. However, pincode of the location was encoded within an image that only Hexagon could decipher. Our recon team relayed this information to us, and now we are tasked with precisely identifying the location. Once determined, our team will proceed to the site and eliminate the remaining enemy forces. 
#### Solution
Reverse search the given png image on https://yandex.com We get the clear image,in image there is a url, opening the url we find the location on the address section

## Grounded
### Description:
Hexagon has decided where to attack the next. He only attacks centre of administration of a country. We have intercepted his travel logs from one of our spy. Going through his travel logs, we came across a picture of a socket. Help our team to identify, where is he going to attack ?

mysterysocket.png

Note: Enter the flag as CTF{<answer>} with spaces replaced by '_'
#### Solution
The socket given in image used in Israel , The central administration of the country is Jerusalem which is the flag

## HelicopterrHelicopterr
### Description: 
You have received a secret message from a squadron of the rebel alliance on Pheins:

T25lIG9mIG91ciBjcnVjaWFsIGxvY2FsIHRyYW5zcG9ydGF0aW9uIHZlaGljbGUgd2FzIH N0b2xlbiEgSGVscCB1cyBmaW5kIHRoZSBjdXJyZW50IG93bmVyL293bmVycyBvZiB0a GUgaGVsaWNvcHRlciB0byBnZXQgdG8gdGhlIHRoZWlmLgooSWYgdGhlcmUgYXJlIH R3byBvd25lcnMgdGhlbiBjb21iaW5lIHRoZWlyIG5hbWVzIHRvIGdldCB0aGUgZmxhZwo gRWcuIGZvciBSaXlhIE1hbm9qIGFuZCBTdGFuIFBoaWxpcCB0aGUgZmxhZyBpcyBSa XlhX1N0YW4pCg==

#### Solution
given secret seems to be base64, decoding it 
```
One of our crucial local transportation vehicle was stolen! Help us find the current owner/owners of the helicopter to get to the theif.
(If there are two owners then combine their names to get the flag
 Eg. for Riya Manoj and Stan Philip the flag is Riya_Stan)
```
from the given image we find aircraft number , using that number we find the company that owns the aircraft on https://opencorporates.com/companies/us_ak/10019092 the flag was the names of the owners

## Crypto Zoo
### Description:
Could you please help me find the transaction ID for a recent transfer of 1,000,000,000 DX from the hacker's wallet that occurred on November 26, 2020? The funds were stolen from Kucoin, a well-known cryptocurrency exchange.

Note: Enter the flag as CTF{<answer>}.
#### Solution
I found trading information about DX in https://coinmarketcap.com/currencies/dxchain-token/. There is a link called Explorer there that redirects you to https://etherscan.io/token/0x973e52691176d36453868D9d86572788d27041A9.

On this page, it is possible to download a CSV with the trade history for this coin. Looking at the date of November 26, it was possible to find the following line:
"0xfdef5b6f6dece6b29695b9fd8d0cadaff944876e598fd443125e1f8c2db15160","11333292","1606384469","2020-11-26 09:54:29","0xd32dbed0609ac3169cc4dd6b781f04cee5ba9550","0xa1d8d972560c2f8144af871db508f0b0b10a3fbf","100000000"

So the flag is:

CTF{0xfdef5b6f6dece6b29695b9fd8d0cadaff944876e598fd443125e1f8c2db15160}
# Miscellaneous
## M336
### Description:
Our bot is very friendly ... just ask FLAG .. but it only responds to !!!!!!!!!!

Note: Ask our bots, in the designated channels.
#### Solution
ask flag to bot on discord using ```!flag```

# Forensics
## James Webb
### Description:
We have come across an image file from a covert channel called HexagonFlags, which is known for discreetly transporting flags. Can you analyze the image and see if you can find any useful information?
![flag](https://github.com/aayushdangol16/HexHimalaya_CTF_Write_Up/blob/main/photo/flag.jpg)
#### Solution
use https://www.aperisolve.com/ to get flag hidden on the image
## Radio Head
### Description:
Your team has sent you an email with an audio file that they are unable to understand. They have forwarded the file to you because you possess expertise in analyzing audio files. Your task is to uncover any hidden message within the file and provide assistance to your team.

(Use underscores in place of spaces.)

Note: Write the flag as CTF{<answer>} with spaces replaced by '_'
#### Solution
use audacity spectogram to find the flag hidden in the given audio file
## Black Box
### Description:
Your team has assigned you the responsibility of infiltrating the enemy's server, and after extensive effort, your team has successfully gained access. Within the server, a folder has been discovered. Now, your team has tasked you with extracting all available information from this file, as they are aware that it contains significant and valuable data.
#### Solution
unzip the given zip file there is a image and two pdf file protected by a password. extract the metadata of image 
```
mu : E09B4AFC22A3E578D77A90D73363C8A5
pwd : EFBE43500C80151A5D7608400FD21BB9
```
decode the mu and pwd 
```
en3my
def3nd3r
```
use this decoded password to open pdf file. on Beta_msg.pdf some text where redact. copy all the text ``` ctr + a ``` and paste on a text file then redact text will be visible,it contain some portion of the flag. on Mu_msg.pdf there is a image of morse code, decode it to get remaining portion of flag, merge two portion to get the flag.
## Base HEx
### Description:
Robot16, your secret agent operating within the enemy base, possesses vital information that could significantly influence the outcome of the war in your favor. Unfortunately, Robot16 is currently experiencing internal problems that prevent it from translating the information. However, Robot16 managed to bring back a file. Your urgent task is to decipher the contents of this file and extract the crucial information before time runs out.
#### Solution
unzip the given zip file which contain  2 pdf file(one is password protected) , image file and a zip file. open op3nm3_f1r5t.pdf it contain
```
OP3NM3_F1R5T
This file contains the main part of the key to find the flag
for this question.
You must solve these both questions to find the hint
1) A word is given to you, rotate it like Julius Caesar with 
the help of the robot. The word is : m4b
2) A word is given to you, rotate it like Julius Caesar with 
the help of the robot. The word is : pev
Combine both these answers to get your hint for this question.
Note : Numbers are numbers.
```
solving this we get ```c4rful ``` which was the name of the image. using this open aft3r_fir5t.pdf , some text were hidden copy all the text and paste on a text-file
hidden text will be visible
```
Welcome!!
Welcome!!!
I appreciate your effort for finding the password for
this file
THis document doesn’t helps you.
```
haha this document doesn't helps you, lets unzip the zip file which contain 123 text file. there is a file named ``` File-c4rful``` opening it there is a password and url
```
https://www.pelock.com/products/steganography-online-codec####
PASSWORD:4416
```
using it we will get our flag
## Area 51
### Description:
As the leader of your team, you embark on a mission to seize the enemy's concealed fortress. Stay vigilant for guards who possess swift reflexes, a commanding presence, and advanced stealth technology. They have Malbolge, a language that is difficult to understand, and they are not afraid to use it. You must find a way to infiltrate the fortress and retrieve the flag.
#### Solution
text file is given in this challange that contain strings. https://malbolge.doleczek.pl/ used to get the drive link 
```
https://drive.google.com/drive/folders/1gOkKD88UlEnx_OxOh-NDDEGwTP8Wkszb?usp=sharing
```

