# Test Cases – FIT4012 Lab 2

## Caesar Cipher

- [x] TC1: Encrypt `I LOVE YOU` với key `3` → "L ORYH BRX" **PASS**
- [x] TC2: Encrypt `hello world` với key `5` → "mjqqt btwqi" **PASS**
- [x] TC3: Decrypt `LORYH BRX` với key `3` → "I LOVE YOU" **PASS**

## Rail Fence Cipher

- [x] TC4: Encrypt `I LOVE YOU` với `2` rails → "ILV OOEYU" **PASS**
- [x] TC5: Encrypt `I LOVE YOU` với `4` rails → "I  EYLVOOU" **PASS**
- [x] TC6: Decrypt `ILV OOEYU` với `2` rails → "I LOVE YOU" **PASS**

## Input Validation & File Input

- [x] TC7: Invalid input (numbers) → Error message **PASS**
- [x] TC8: Invalid input (special chars) → Error message **PASS**
- [x] TC9: Read from `data/input.txt` and encrypt **PASS**
