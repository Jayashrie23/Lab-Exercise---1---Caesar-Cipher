# Lab-Exercise---1---Caesar-Cipher

## Aim : 
To encrypt and decrypt the given message by using Ceaser Cipher encryption algorithm.

## Procedure :
1. Design of Caeser Cipher algorithm.
2. Implementation using C or pyhton code. 
3. In Ceaser Cipher each letter in the plaintext is replaced by a letter some fixed number 
of positions down the alphabet. 
4. For example, with a left shift of 3, D would be replaced by A, E would become B, and 
so on.  
5. The encryption can also be represented using modular arithmetic by first transforming the letters into numbers, according to the scheme, A = 0, B = 1, Z = 25. 
6. Encryption of a letter x by a shift n can be described mathematically as, En(x) = (x + n) mod26
7. Decryption is performed similarly,Dn (x)=(x - n) mod26.

## Program :
```
def caesar_cipher(text, shift):
    result = ""

    for char in text:
        if char.isupper():
            result += chr((ord(char) - ord('A') + shift) % 26 + ord('A'))
        elif char.islower():
            result += chr((ord(char) - ord('a') + shift) % 26 + ord('a'))
        else:
            result += char  # Keep spaces, numbers, and punctuation unchanged

    return result


choice = input("Encrypt or decrypt? (e/d): ").lower()
message = input("Enter your message: ")
shift = int(input("Enter shift value: ")) % 26

if choice == "d":
    shift = -shift
elif choice != "e":
    print("Invalid choice.")
    raise SystemExit

print("Result:", caesar_cipher(message, shift))
```

## Output :
<img width="1330" height="1015" alt="image" src="https://github.com/user-attachments/assets/459c7835-213e-4261-b4e8-0bdaa7d35a22" />


## Result :
The program is executed successfully.
