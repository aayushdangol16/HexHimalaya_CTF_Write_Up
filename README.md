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
![jamess](https://github.com/aayushdangol16/HexHimalaya_CTF_Write_Up/blob/main/photo/james.png)
## Radio Head
### Description:
Your team has sent you an email with an audio file that they are unable to understand. They have forwarded the file to you because you possess expertise in analyzing audio files. Your task is to uncover any hidden message within the file and provide assistance to your team.

(Use underscores in place of spaces.)

Note: Write the flag as CTF{<answer>} with spaces replaced by '_'
#### Solution
use audacity spectogram to find the flag hidden in the given audio file
![radio](https://github.com/aayushdangol16/HexHimalaya_CTF_Write_Up/blob/main/photo/radio.png)
## Black Box
### Description:
Your team has assigned you the responsibility of infiltrating the enemy's server, and after extensive effort, your team has successfully gained access. Within the server, a folder has been discovered. Now, your team has tasked you with extracting all available information from this file, as they are aware that it contains significant and valuable data.
#### Solution
unzip the given zip file there is a image and two pdf file protected by a password. extract the metadata of image 
![black](https://github.com/aayushdangol16/HexHimalaya_CTF_Write_Up/blob/main/photo/Black_Box.png)
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
After a quick bit of Googling, I found that, this text is Malbolge code. So I compiled it with Malbolge Online Compiler and upon execution I got this link.
```
https://drive.google.com/drive/folders/1gOkKD88UlEnx_OxOh-NDDEGwTP8Wkszb?usp=sharing
```
download image from the link
![allll](https://github.com/aayushdangol16/HexHimalaya_CTF_Write_Up/blob/main/photo/Finf_me.png)
After some adjustments in above picture we got 4 QR codes https://www.aperisolve.com/
![qr](https://github.com/aayushdangol16/HexHimalaya_CTF_Write_Up/blob/main/photo/qr.png) <br />
By scanning QR codes we got links and combined those links to get another picture. Finally, that contained our Flag. But we had to use Superimposed image to see the hidden flag. <br />
![su](https://github.com/aayushdangol16/HexHimalaya_CTF_Write_Up/blob/main/photo/su.png)
## Bomb
### Description:
UnZip, Check, Repeat
#### Solution
In a challange we have been given a zip file. Name of the zip file was ``` Zipped2048``` inside that zip file there is another zip file named ``` Zipped2047```.The number in the file is like there is 2048 zip file, its like we have to unzip all that zip so lets automate
```
from zipfile import ZipFile
import os
os.chdir("boom")
i=0
while(i<2048):
    a=os.listdir()
    i=i+1
    print(a[0])
    with ZipFile(a[0], 'r') as zip:
        zip.printdir()
        zip.extractall()

```
after unzipping all the zip there contain a txt file which have our flag.
## Come Back
### Description:
Git is very good friend ! It commits our previous data also.
#### Solution
In a challange we have been given a zip file. It contain ```.git``` lets go through git
``` git log ``` <br />
![log](https://github.com/aayushdangol16/HexHimalaya_CTF_Write_Up/blob/main/photo/gitlog.png) <br /> <br />
``` git show 864c3eacfff68dd1a4ec570836213ee6afbebdf3 ``` </br></br>
![log](https://github.com/aayushdangol16/HexHimalaya_CTF_Write_Up/blob/main/photo/gitshow.png)
# Web Exploitation
## Robots
### Description:
Have you ever heard of bots crawling through the internet??
#### Solution
We have given a ```https://hexrobots.netlify.app/``` From the challange name ```robots``` its like a robots.txt go to ```https://hexrobots.netlify.app/robots.txt``` there is a path ```https://hexrobots.netlify.app/10122003.html``` go to that path we will get our flag
## Never Gonna Give You Up
### Description:
Find what is in between the files.
#### Solution
we have given a link ``` https://hex-nevergonnagiveyouup.netlify.app/1.html``` while opening that link it will redirect to ```https://hex-nevergonnagiveyouup.netlify.app/2.html``` then ```https://hex-nevergonnagiveyouup.netlify.app/3.html``` and finally it will redirect to youtube video. view the source code ```view-source:https://hex-nevergonnagiveyouup.netlify.app/2.html``` flag is ready for you :)
## Fast as Flash
### Description:
URGENT HEx-Team,
One of the prisoners in the space prison has hacked into the Hexagon educational website and we suspect they have left a message for us. We need your assistance in locating it.
```https://hex-education.netlify.app/```
Best of luck, HQ
#### Solution
In a js file ```https://hex-education.netlify.app/assets/js/flash.js``` there is a Hex encoded string
```
function changeText() {
  var _0x10b01e = _0x3feceb;
  (document["querySelector"](_0x10b01e(0x74))[_0x10b01e(0x79)] = hex2a(
    "4354467B57335F525F5337314C4C5F483352337D"
  )),
    (document[_0x10b01e(0x76)](_0x10b01e(0x74))["style"]["fontSize"] = "50px");
}
```
```
4354467B57335F525F5337314C4C5F483352337D
```
decode it flag is ready for you
## Grandma's Cookie
### Description:
HQ,

Reconnaissance has uncovered an outdated HEx Galactics website, which may potentially contain an insecure administration portal. Requesting your assistance in investigating the website for any vulnerabilities. Historically, HEx Galactics has not been known for employing top-tier developers.
```https://hex-galactics.netlify.app/```
Awaiting your findings, HQ

#### Solution
Go to ```view-source:https://hex-galactics.netlify.app/``` there is ```admin.html```. In ```https://hex-galactics.netlify.app/admin.html``` put random username and password it says<br/> 
```
INVALID LOGIN CREDENTIALS
PLEASE LOGIN AS ADMIN
```
lets check js code ```https://hex-galactics.netlify.app/js/script.js```
```
form.addEventListener('submit', (e) => {
    e.preventDefault();
    let username = document.getElementById('username').value;
    if (document.cookie === '') {
        document.cookie = "admin=false";
        document.cookie = `user=${username}`;
        window.location = "denied.html" // Redirect
    }
    else {
        let admin = getCookie("admin");
        if (admin === "true") {
            window.location = "panel.html"; // Redirect
        }
        else {
            window.location = "denied.html" // Redirect
        }
    }
});
```
in cookie if admin=true and user=admin then we will redirect to ```panel.html``` so lets manipulate the request<br/>
![brup](https://github.com/aayushdangol16/HexHimalaya_CTF_Write_Up/blob/main/photo/burp.png)
yahh we got ```js/solved.js```it contain base64 encoding
```
const first = "Q1RGe2J1Ny03a";
const second = "DMtbTFMay1qdTU3LW";
const third = "ZsMDRUNS00VzR5IX0=";
```
```Q1RGe2J1Ny03aDMtbTFMay1qdTU3LWZsMDRUNS00VzR5IX0=``` decode it we will get flag
## HEx Mainframe
### Description:
Your team has been tipped by one of the rebels of a weak vulnerability in HEx' mainframe database. Pretending to be HEx', crack the password, and breach into its mainframe where classified information is stored. Be careful though, as HEx’ robots are always on high alert and they keep changing the password.
Link:```https://hex-mainframe.netlify.app/```
#### Solution
view the page source,there is a python code which is commented
```

        import hashlib

        def hash_pw(pw_str):                         
            pw_bytes = bytearray()
            pw_bytes.extend(pw_str.encode())
            m = hashlib.md5()
            m.update(pw_bytes)
            return m.digest()
```
i guess this code is been used for hashing the password.lets move forward, from ```https://hex-mainframe.netlify.app/robots.txt``` we will get two file
```
 /records.html
 /3outof3.html
```
from ```https://hex-mainframe.netlify.app/records.html``` we will get list of possible passwords,downloading possible passwords file may be helpfull on further
from ```https://hex-mainframe.netlify.app/script.js``` we get ```//correct hash is b'\x00u@3 (1/3)``` 
from ```https://hex-mainframe.netlify.app/style.css``` we get ```/* \xde\x19dD\xc1\tO (2/3) */```
from ```https://hex-mainframe.netlify.app/3outof3.html``` we get ```\x9d\x9f\xf45\x8f' (3/3)```
combining above hash ```\x00u@3\xde\x19dD\xc1\tO\x9d\x9f\xf45\x8f``` it is correct hash from possible passwords, now from possible passwords, hash it and compare to ```\x00u@3\xde\x19dD\xc1\tO\x9d\x9f\xf45\x8f``` we will get password. lets write some script
```
import hashlib
i=0
a=open("file.txt","r")
s=a.read()
s = s.replace("'", "") 
s=s.replace(" ","") 
name_list = s.split(",")  
def hash_pw(pw_str):
    pw_bytes = bytearray()
    pw_bytes.extend(pw_str.encode())
    m = hashlib.md5()
    m.update(pw_bytes)
    return m.digest()


while(i<len(name_list)):
    pwhash=hash_pw(name_list[i])
    if pwhash == b'\x00u@3\xde\x19dD\xc1\tO\x9d\x9f\xf45\x8f':
        print("yes found")
        print(name_list[i])
        exit(0)
    i=i+1

```
password is ```34r7h```
from ```https://hex-mainframe.netlify.app/script.js``` username is ```HEX``` we got username and password login it grab the flag
#Cryptography
## Dora Milaje
### Description:
You have received a secret message from your commander containing instructions disguised with the phrase "from the lands of vibranium." Decrypt the code and proceed accordingly.

Note: Enter the flag as CTF{<answer>} with spaces replaced by '_'
![dora](https://github.com/aayushdangol16/HexHimalaya_CTF_Write_Up/blob/main/photo/dora.png)
#### Solution
In this challenge I found that the problem name Dora milaje is some How related to the fictional world wakanda from a marvel moive as a phrase “from the lands of vibranium"
Mentioned. So I google about the letters in this script and there corresponding alphabets in English language and I was able to found this <br/>
![dora1](https://github.com/aayushdangol16/HexHimalaya_CTF_Write_Up/blob/main/photo/dora1.png)<br/>
From this I was able to decode the given code as:
RIP Chadwick Boseman since Chadwick was the main character in this world and he is no more I was sure it is the required flag

## Long Base
### Description:
At the age of 16, my grandfather drove me to a base located next to house number 64. While there, I came across a mysterious message. My grandfather assured me that I would eventually discover its meaning. Can you assist my younger self in decrypting this message? 襃𠅆時鑧 𓁢𓈰 桨鑲鬰靟 𓄴 鐳椶 ᕽ
#### Solution
In this challenge, we were given some Chinese like digits and some Egyptian symbols. After a quick bit of googling, I found that these were Base65536 codes. So, I went to this website
https://www.better-converter.com/Encoders-Decoders/Base65536-Decode . Decoding from this site we got our flag<br/>
![bb](https://github.com/aayushdangol16/HexHimalaya_CTF_Write_Up/blob/main/photo/bbbb.png)

## The Imitation Game
### Description:
Attention! You have been informed by your allies that there exists a crucial code that, once decrypted, could significantly aid in winning the war. Furthermore, you've learned that these types of codes were prominently employed during ancient human conflicts that transpired several decades ago. If you possess the skill and determination to become the Alan Turing of this war, unravel the code and seize the opportunity.

XKQKZOHUARFUEUQUBGFUFTJJHSAWVCFDRKZJG
#### Solution

In this challenge, we were given some codes. As the topic was the imitation game, I remembered about the world war and movie. So, I went to popular website dcode.fr ```https://www.dcode.fr/en ```.
I chose the tool as enigma machine and got the Flag.<br/>
![nepal](https://github.com/aayushdangol16/HexHimalaya_CTF_Write_Up/blob/main/photo/nepal.png)<br/>

## Breaking Bad
### Description:
You discover that dangerous chemical weapons are being transported to the enemy base with the intention of using them against you and your allies. Taking matters into your own hands, you manage to seize the supplies, only to find that they are securely locked in a container that requires a passcode to open. Given the nature of these chemicals, it is crucial to handle them safely, and having some knowledge in chemistry will be advantageous. It is important to remember that all substances are made up of elements, each possessing unique chemical and physical properties, and they cannot be transformed into different substances through typical chemical reactions. As a chemistry enthusiast, your task is to decrypt the passcode.

1 AD 53 EG 45 84 39 22 E 7 T 8 53 A 15 L

1 59 53 47 113 84 85 23 E 7 T 15 53 73 L

P.S.- Prime numbers are exceptional indices 😁
#### Solution
I arranged the both row of passcode by replacing the number by the elements symbol and find the common words in both rows i.e:

```
HADIEGRHPOYTIENTOIAPL

HPRIAGNHPOATVENTPITAL

COMMON:HIGHPOTENTIAL
```

```FLAG:CTF{HIGHPOTENTIAL}```

## Dark Storm
### Description
The enemy has launched an artificial hurricane in the path of your allies, with the help of a computer network named AE23444, kept hidden in a safe location at Beaufort. You have to measure the wind speed to analyze where the computer is. Decode the hidden message with the help of HEX to win the war. The message is:<br/>
![dark](https://github.com/aayushdangol16/HexHimalaya_CTF_Write_Up/blob/main/photo/dark.png)<br/>
Note: Enter the flag as CTF{<answer>} with spaces replaced by '_'
#### Solution

Here  the message was in the form of color Alphabet and it was decode by using  this refrence:<br/>
![dark1](https://github.com/aayushdangol16/HexHimalaya_CTF_Write_Up/blob/main/photo/dark1.png)<br/>
<br/>And found to be DGT TZ EAA FOQGV the it was decoded as:<br/>
![dark2](https://github.com/aayushdangol16/HexHimalaya_CTF_Write_Up/blob/main/photo/dark1.png)<br/>
FLAG:CTF{ EYE_OF_THE_STORM}
