<h1>Simple Encryption Maker Lab</h1>

<h2>Description</h2>
This is a simple Python script that takes inspiration from the common Caesar Cipher encryption model. The script first imports the string module. Next, it defines a function called "encrypt" which takes two parameters, the text to be encrypted and the key (shift value). Inside the function, it creates an empty string that will be used to store the encrypted text. It iterates through each character in the text, checking if the character is a letter, if true, it shifts the letter by the key using ord() and chr() functions. Then it adds the shifted letter to the encrypted text. Finally, it returns the encrypted text. It then tests the function by defining a text and key value and calls the function, encrypting the text, and printing the encrypted text.
<br />


<h2>Languages and Utilities Used</h2>

- <b>Python</b> 

<h2>Environments Used </h2>

- <b>Windows 11</b>

<h2>Program Code:</h2>
 
 ```python
 # Step 1: Import the necessary modules
import string

# Step 2: Define the encryption function
def encrypt(text, key):
    # Step 2.1: Create an empty string to store the encrypted text
    encrypted_text = ""
    # Step 2.2: Iterate through each character in the text
    for char in text:
        # Step 2.3: Check if the character is a letter
        if char.isalpha():
            # Step 2.4: Shift the letter by the key
            char = chr((ord(char) + key - 97) % 26 + 97)
        # Step 2.5: Add the shifted letter to the encrypted text
        encrypted_text += char
    # Step 2.6: Return the encrypted text
    return encrypted_text

# Step 3: Test the encryption function
text = "Hey guys my name is Denal!"
key = 3
encrypted_text = encrypt(text, key)
print(encrypted_text)
print(text)
```
