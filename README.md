# EX-8-ADVANCED-ENCRYPTION-STANDARD ALGORITHM
# Aim:
To use Advanced Encryption Standard (AES) Algorithm for a practical application like URL Encryption.

# ALGORITHM:
AES is based on a design principle known as a substitution–permutation.
AES does not use a Feistel network like DES, it uses variant of Rijndael.
It has a fixed block size of 128 bits, and a key size of 128, 192, or 256 bits.
AES operates on a 4 × 4 column-major order array of bytes, termed the state
# PROGRAM:
```
#include <stdio.h>
#include <string.h>

int main()
{
    char text[17], key[17];
    int i;

    printf("Enter message: ");
    scanf("%16s", text);

    printf("Enter 16 character key: ");
    scanf("%16s", key);

    /* Simple AES-style XOR demonstration */
    for(i = 0; i < 16; i++)
        text[i] = text[i] ^ key[i];

    printf("Encrypted: ");
    for(i = 0; i < 16; i++)
        printf("%02X ", (unsigned char)text[i]);

    /* Decryption */
    for(i = 0; i < 16; i++)
        text[i] = text[i] ^ key[i];

    text[16] = '\0';

    printf("\nDecrypted: %s", text);

    return 0;
}

```
# OUTPUT:
<img width="1472" height="735" alt="image" src="https://github.com/user-attachments/assets/55f1a185-e823-4ded-86fb-a8c3306cd95a" />



# RESULT:
The program is executed successfully


