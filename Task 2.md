## Task 2 - PicoCTF

### 1)Binary Exploitation
**1.Stonks**:

>The API token is gettting printed back from the stack
>
>![image](https://user-images.githubusercontent.com/118385974/222921837-993033fe-a044-49af-b242-a27c97fb82e4.png)
>
>![image](https://user-images.githubusercontent.com/118385974/222922022-247be00a-56ec-4ee2-bb1b-1ce6306f6386.png)
>
>So I used couple of %x to print from the stack
>![image](https://user-images.githubusercontent.com/118385974/222922152-0deca362-0813-4074-8826-8cd1527a2c7e.png)
>
>I ran the output through a hexadecimal to ASCII converter to get ocip{FTC0l_I4_t5m_ll0m_y_y3nbc7ceac6ÿ}
>
>Learnt that flag has been organized in big endian and converted it to little endian by reversing four characters at a time to get the flag.

**2.Cache Me Outside**

### 2)Cryptography
**1.Mod 26**:

>![image](https://user-images.githubusercontent.com/118385974/222922387-d4753dba-ea6b-4f8d-8c97-ab7537b3dc1c.png)
>
>Ran the flag through a Rot13 converter which shifts each letter by 13 places in the alphabet.

### 3)Web Exploitation

### 4)Forensics

### 5)General Skills

### 6)Reverse Engineering
