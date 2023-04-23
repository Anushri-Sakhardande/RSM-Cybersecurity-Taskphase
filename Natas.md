# NATAS Writeup


## Level 0

The password was in the comments of the HTML 

![image](https://user-images.githubusercontent.com/118385974/233842160-b37210f0-1a56-4cd2-a6b5-91e58ea0911f.png)

The password for natas1 is g9D9cREhslqBKtcA2uocGHPfMZVzeFK6 



## Level 0 --> level 1

![image](https://user-images.githubusercontent.com/118385974/233842144-e1d3cf44-b9b2-4b78-bd46-f7ec5c8c8905.png)

Right clicking is blocked so I used Ctrl+U to access the dev tools

The password for natas2 is h4ubbcXrWqsTo7GGnnUMLppXbOogfBZ7 



## Level 1 --> level2

![image](https://user-images.githubusercontent.com/118385974/233842135-1c34ca4b-30c8-4a8f-b301-bde03727fff7.png)

There is a directory named files so we navigate to it

![image](https://user-images.githubusercontent.com/118385974/233842128-4572602a-ff98-4532-8ca7-df3e57e4f3c9.png)

There is a text file called users.txt containing the password for natas3

![image](https://user-images.githubusercontent.com/118385974/233842116-85368fee-6352-40c1-bda5-54436f799a7d.png)

natas3:G6ctbMJ5Nb4cbFwhpMPSvxGHhQ7I6W8Q


## Level 2 --> level 3

![image](https://user-images.githubusercontent.com/118385974/233842101-3843ad84-716c-4e39-8024-92a21a4aa1f1.png)

There is a clue directing that Google can’t find so I checked the robots.txt file which is used by web crawlers (a robot used by search engines while looking for keywords) 

![image](https://user-images.githubusercontent.com/118385974/233842087-04ae03c4-e20c-4f71-831b-2f2621101f81.png)

The file shows that there exists a directory called /s3cr3t/

![image](https://user-images.githubusercontent.com/118385974/233842077-cb5de1a1-4554-4cc5-bfa9-964362a0c88c.png)

This has a file called users.txt containing the password

natas4:tKOcJIbzM4lTs8hbCmzn5Zr4434fGZQm



## Level 3 --> level 4

![image](https://user-images.githubusercontent.com/118385974/233842062-6117c0a3-4e0c-4522-bea1-520e67abd0dd.png)

The clue given says that the reference should be http://natas5.natas.labs.overthewire.org/

![image](https://user-images.githubusercontent.com/118385974/233842049-08c87901-edb2-4617-bf22-65508e837ce9.png)

I intercepted the request using BurpSuite, changed the referer to natas5 and forwarded the request.

![image](https://user-images.githubusercontent.com/118385974/233842024-5d82a60e-326d-4a51-8320-9907f90753c1.png)

The password for natas5 is Z0NsrtIkJoKALBCLi5eqFfcRN82Au2oD



## Level 4 -> level 5

![image](https://user-images.githubusercontent.com/118385974/233842016-d411f5d0-8aee-49b3-81a8-add64981dba7.png)

The clue says we arent logged in so I again intercepted the request using Burp Suite

![image](https://user-images.githubusercontent.com/118385974/233842001-047ef657-87bb-4e08-aa48-54694a3a5a74.png)

I changed the loggedin from 0 to 1

![image](https://user-images.githubusercontent.com/118385974/233841986-2b0a5bbf-1a0d-4399-a95a-1606969de6a7.png)

The password for natas6 is fOIvE0MDtPTgRhqmmvvAOt2EfXR6uQgR



## Level 5 --> level 6

![image](https://user-images.githubusercontent.com/118385974/233841809-20737e78-7715-4323-a2e3-83e21706b16a.png)

Sourcecode contains the following code

![image](https://user-images.githubusercontent.com/118385974/233841834-05ac21ed-e410-4b9f-9d45-2f0bd680f8bf.png)


They are importing a directory called  “includes/secret.inc” so I navigated to it and found the secret

![image](https://user-images.githubusercontent.com/118385974/233841796-ceec5c0f-beba-4634-a4ec-cc1192b00c0e.png)

<?
$secret = "FOEIUWGHFEEUHOFUOIU";
?>

And password is then revealed

![image](https://user-images.githubusercontent.com/118385974/233841775-3967d9f4-2274-4d33-9801-c95764775ee0.png)

The password for natas7 is jmxSiH3SP6Sonf8dv66ng8v1cIEdjXWr


## Level 6 --> level 7

![image](https://user-images.githubusercontent.com/118385974/233842387-cdefb65f-d725-4f09-ae37-c473956d8f1d.png)

Site contains two pages

![image](https://user-images.githubusercontent.com/118385974/233842422-6d1b303b-295f-4c6a-a9b0-eb0058be19ab.png)

Hint is provided that the password for the user natas8 is in the given directory, So we change the request as

![image](https://user-images.githubusercontent.com/118385974/233842839-4b15923a-a1fc-4124-a337-a234abaaa131.png)

To obtain the password

a6bZCNYwdKqN5cGP11ZdtPg0iImQQhAB


## Level 7 --> level 8

![image](https://user-images.githubusercontent.com/118385974/233842900-08020e0f-7a6e-4eb1-bc22-0aa33c98ed91.png)

We again have a secret input 

![image](https://user-images.githubusercontent.com/118385974/233842947-694ba83b-0544-475c-bb0c-9511e170773d.png)

We have a secret which we must decode


