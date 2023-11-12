# SPM -Secure Password Manager-
#### Video Demo:  https://www.youtube.com/watch?v=tbkujlfDuUk
#### Description:
This app is a terminal-based password manager so it can be used in Linux, Windows, and Mac. It has its own local database. All people who use the computer can use it safely because it has an account system.
I wrote this app for the CS50x final project. It may have bugs.

![login menu][resim]

[resim]: ./menu.png "Login Menu"

## USAGE
1. You have to have Python. If you haven't downloaded it before, download it. [Python](https://www.python.org/downloads/)
2. Open the terminal
3. Write this if necessary ```pip install bcrypt``` (Download necessary libraries if you don't have.)
4. Write ``` python3 password_manager.py```
5. It's done, you can do whatever you want.

![functions][resim2]

[resim2]: ./funcs.png "Functions"
#### These are what you can do.

### This app uses these libraries.
If you have a problem with libraries, you can use the "pip" command in your terminal, and download these libraries.
1. sqlite3
2. bcrypt
3. base64
4. Fernet
5. Figlet

### Working Principle
This app has its own local database. Users can create different accounts on one computer. It hashes the main password, and other passwords encrypting.  It uses bcrypt library, and Brcrypt uses the "Blowfish algorithm" for hashing.  For encryption and decryption, it uses the Fernet library, and Fernet uses the "AES algorithm". AES is a strong symmetric key encryption method.

This code has 5 main files and 1 database in a directory.
The first is password_manager.py. It includes login and sign-in functions. Also, it creates a user key and this key is used in almost every database function.
functions.py has functions for hashing, decrypting, encrypting, adding passwords, reading passwords, etc.
main_menu.py is the menu that is used for selecting what you want to do.
sql_queries.py provides a connection with the database. It creates a database if it didn't exist before. It has two tables: accounts and passwords. Former incudes user datas. Latter includes passwords.
title_maker.py just has a show function. It writes the title when the app starts. Also, it makes a box for important information.
#### INFOs about used algorithms from ChatGpt
#### Blowfish Algorithm
The Blowfish algorithm is a symmetric key block cipher designed by Bruce Schneier in 1993 as a fast and secure alternative to existing encryption algorithms. Known for its simplicity and efficiency, Blowfish operates on fixed-size blocks of data, encrypting or decrypting 64-bit blocks at a time. One of its distinctive features is the variable key length, ranging from 32 to 448 bits, making it adaptable to various security requirements. Blowfish employs a Feistel network structure, dividing the input block into two halves and iteratively applying a function to mix these halves. Its key expansion process generates a set of subkeys derived from the user-provided key, enhancing the algorithm's resistance against various cryptographic attacks. While Blowfish was widely adopted in the 1990s and early 2000s, it has been largely succeeded by more recent algorithms like AES. Nonetheless, its influence persists, and it remains a valuable historical contribution to the field of symmetric key cryptography.
#### AES algorithm
The Advanced Encryption Standard (AES) stands as a cornerstone in modern cryptography, serving as a widely adopted symmetric key encryption algorithm. Established by the National Institute of Standards and Technology (NIST) in 2001, AES replaced the aging Data Encryption Standard (DES) to address its vulnerabilities. AES operates on blocks of data, employing a substitution-permutation network that involves multiple rounds of transformation. Key strengths of AES lie in its flexibility and security. It supports key sizes of 128, 192, and 256 bits, providing a balance between efficiency and robustness. The algorithm's strength is attributed to its resistance against various cryptographic attacks, including differential and linear cryptanalysis. As a result, AES has become the de facto standard for securing sensitive information across diverse applications, from secure communication protocols to data storage and financial transactions. Its ubiquity underscores its reliability and effectiveness in safeguarding digital data in today's interconnected world.


##### This app was written by Abdullah Enes Solak.
##### 10.11.2023
##### Ankara, Turkey
