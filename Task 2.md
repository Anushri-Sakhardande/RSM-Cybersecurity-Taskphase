# Task 2 - PicoCTF

LINK FOR LONGER VERSION:https://docs.google.com/document/d/1LDM6YegyXL2H1EFFvlkf6xdiQluPFk2W9m2wpB33HK4/edit?usp=sharing

## 1)Binary Exploitation

### 1.Stonks:

The API token is gettting printed back from the stack.

![image](https://user-images.githubusercontent.com/118385974/222921837-993033fe-a044-49af-b242-a27c97fb82e4.png)

![image](https://user-images.githubusercontent.com/118385974/222922022-247be00a-56ec-4ee2-bb1b-1ce6306f6386.png)

So I used couple of %x to print from the stack.

![image](https://user-images.githubusercontent.com/118385974/222922152-0deca362-0813-4074-8826-8cd1527a2c7e.png)

I ran the output through a hexadecimal to ASCII converter to get ocip{FTC0l_I4_t5m_ll0m_y_y3nbc7ceac6ÿ}

Learnt that flag has been organized in big endian and converted it to little endian by reversing four characters at a time to get the flag.


### 2.Cache Me Outside



## 2)Cryptography

### 1.Mod 26:

![image](https://user-images.githubusercontent.com/118385974/222922387-d4753dba-ea6b-4f8d-8c97-ab7537b3dc1c.png)

Ran the flag through a Rot13 converter which shifts each letter by 13 places in the alphabet.


### 2.Mind your Ps and Qs:

Read up about RSA encryption. 

![image](https://user-images.githubusercontent.com/118385974/222922659-7eed40bb-0ae8-4f8c-923f-21ff56d7a2c4.png)

Used an online converter to find factors and convert the message.

![image](https://user-images.githubusercontent.com/118385974/222922645-5cc6c3b6-580b-4ca7-b22f-a274be0d20b1.png)



## 3)Web Exploitation

### 1.GET aHEAD:

![image](https://user-images.githubusercontent.com/118385974/222923332-20b24f59-4a78-48e7-a7f6-b13538cb1eb1.png)

![image](https://user-images.githubusercontent.com/118385974/222923413-b6574704-e0ba-4c51-8a09-9e6821a642d9.png)

GET and POST method was used for red and blue respectively. 

![image](https://user-images.githubusercontent.com/118385974/222923348-dcd76b56-6bc6-45c0-86e2-506a96327c4d.png)

Used Postman extension to request method HEAD and found flag in the header.


### 2.Insp3ct0r:

First part was in the HTML of the site.

![image](https://user-images.githubusercontent.com/118385974/222923486-1fb59413-3393-43b1-a444-213696000fc2.png)

Second part was in the CSS.

![image](https://user-images.githubusercontent.com/118385974/222923510-3a67f32b-3841-44df-ad0f-da251ee0d94b.png)

Third part was in the Javascript.

![image](https://user-images.githubusercontent.com/118385974/222923528-c569a72d-004f-4c3d-be3c-fdc19400ac1b.png)



## 4)Forensics

### 1.information:

![image](https://user-images.githubusercontent.com/118385974/222923606-58657c1e-79f2-470e-b946-2ac7eb54df1c.png)

Noticed a base64 encoded text in the details of the cat.jpg.

![image](https://user-images.githubusercontent.com/118385974/222923638-8470d5fb-80b3-4442-b4c5-b6fb14b96e77.png)

decoded it to get the flag.


### 2.Matryoshka doll:

changed the jpg extension to rar and and used an online decompressor each time to get the succesive image till the flag.txt was obtained.

![image](https://user-images.githubusercontent.com/118385974/222923664-f0073be9-266d-4b7b-b103-6304bedfa85f.png)


![image](https://user-images.githubusercontent.com/118385974/222923655-3215d7d4-d3fb-492a-aad3-f452c041fab6.png)



## 5)General Skills

### 1.Python Wrangling:

Looked at the code in which input gets decoded.

![image](https://user-images.githubusercontent.com/118385974/222940027-354fd3c2-cb35-453a-bc3d-4b72dbaf0333.png)

When prompted for password I put in the contents of the pw.txt.

![image](https://user-images.githubusercontent.com/118385974/222923696-95e4f3e3-b6fc-4628-8aac-8f2ef6d1f965.png)


### 2.Wave a flag:

Used the hints to open the ./warm file and then used chmod x+ to get the access and -h again as per the hints.

![image](https://user-images.githubusercontent.com/118385974/222923724-bc7f4aea-4d56-4910-8d05-d2bae1481acb.png)



## 6)Reverse Engineering

### 1.Transformation:

''.join([chr((ord(flag[i]) << 8) + ord(flag[i + 1])) for i in range(0, len(flag), 2)]) 
The code loops through 2 characters at a time from the flag, shifts the first character by two bytes and joined it with the second character is converted to character.

So extracted each character and split the first two bytes and shifted it back by 2 bytes and the second two bytes converted back to character

![image](https://user-images.githubusercontent.com/118385974/222940078-397be231-d830-4ddd-a047-8284245a8815.png)


![image](https://user-images.githubusercontent.com/118385974/222940097-546703fc-61de-4ad6-bac4-f3a6a7222970.png)


### 2.keygenme-py:

Parts of the flag are given

![image](https://user-images.githubusercontent.com/118385974/222974998-18eb6b45-e63b-4b4d-a216-72619674181c.png)

The second encrypted part of the key is checked in this piece of code using the username which is "GOUGH"

![image](https://user-images.githubusercontent.com/118385974/222940118-c35f6cf7-d325-4524-99ff-3dc8ad9fc17f.png)

So I converted the username using the same hashing algorithm to get the flag.

![image](https://user-images.githubusercontent.com/118385974/222940131-03d43d96-9631-4bc0-8139-12f244c1c21c.png)


