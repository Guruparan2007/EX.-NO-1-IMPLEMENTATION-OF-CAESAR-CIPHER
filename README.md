# EX. NO: 1(A) : IMPLEMENTATION OF CAESAR CIPHER
```
NAME: GURUPARAN G
REG NO: 212224220030
```
## AIM:
To implement the simple substitution technique named Caesar cipher using C language.

## ALOGORITHM:

STEP-1: Read the plain text from the user.

STEP-2: Read the key value from the user.

STEP-3: If the key is positive then encrypt the text by adding the key with each character in the plain text.

STEP-4: Else subtract the key from the plain text.

STEP-5: Display the cipher text obtained above.

## PROGRAM:
``` 
#include <stdio.h>
#include <string.h>
#include <ctype.h>
void encrypt(char text[], int shift) {
 for (int i = 0; text[i] != '\0'; i++) {
 char ch = text[i];
 if (isalpha(ch)) {
 char base = isupper(ch) ? 'A' : 'a';
 text[i] = (ch - base + shift) % 26 + base;
 }
 }
}
void decrypt(char text[], int shift) {
 for (int i = 0; text[i] != '\0'; i++) {
 char ch = text[i];
 if (isalpha(ch)) {
 char base = isupper(ch) ? 'A' : 'a';
 text[i] = (ch - base - shift + 26) % 26 + base;
 }
 }
}
int main() {
 char text[100];
 int shift = 3;
 printf("Enter a message: ");
 fgets(text, sizeof(text), stdin);
 encrypt(text, shift);
 printf("Encrypted message: %s", text);
 decrypt(text, shift);
 printf("Decrypted message: %s", text);
 return 0;
}
```
## OUTPUT:
<img width="873" height="483" alt="image" src="https://github.com/user-attachments/assets/d39e24d5-e7dc-4741-b113-0b8761d5e170" />


## RESULT :
 Thus the implementation of ceasar cipher had been executed successfully.
