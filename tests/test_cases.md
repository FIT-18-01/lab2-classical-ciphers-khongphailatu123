# Test Cases – FIT4012 Lab 2

## Caesar Cipher

### TC1: Encrypt `I LOVE YOU` với key `3`
- **Input**: "I LOVE YOU", key = 3
- **Expected Output**: "L ORYH BRX"
- **Status**: ✓ PASS

### TC2: Encrypt `hello world` với key `5`
- **Input**: "hello world", key = 5
- **Expected Output**: "mjqqt btwqi"
- **Status**: ✓ PASS

### TC3: Decrypt `LORYH BRX` với key `3`
- **Input**: "LORYH BRX", key = 3
- **Expected Output**: "I LOVE YOU"
- **Status**: ✓ PASS

## Rail Fence Cipher

### TC4: Encrypt `I LOVE YOU` với `2` rails
- **Input**: "I LOVE YOU", rails = 2
- **Expected Output**: "ILV OOEYU"
- **Pattern**: Rail 0: I, L, V, (space), O; Rail 1: (space), O, E, Y, U
- **Status**: ✓ PASS

### TC5: Encrypt `I LOVE YOU` với `4` rails
- **Input**: "I LOVE YOU", rails = 4
- **Expected Output**: "I  EYLVOOU"
- **Pattern**: Rail 0: I, (space); Rail 1: (space), E, Y; Rail 2: L, V, O; Rail 3: O, U
- **Status**: ✓ PASS

### TC6: Decrypt `ILV OOEYU` với `2` rails
- **Input**: "ILV OOEYU", rails = 2
- **Expected Output**: "I LOVE YOU"
- **Status**: ✓ PASS

## Input Validation

### TC7: Invalid input with numbers
- **Input**: "HELLO123"
- **Expected**: Error message "Invalid input. Only letters and spaces are allowed."
- **Status**: ✓ PASS

### TC8: Invalid input with special characters
- **Input**: "HELLO@WORLD"
- **Expected**: Error message "Invalid input. Only letters and spaces are allowed."
- **Status**: ✓ PASS

## File Input

### TC9: Read from `data/input.txt`
- **File content**: "I LOVE YOU"
- **Action**: Read and encrypt with 2 rails
- **Expected Output**: "ILV OOEYU"
- **Status**: ✓ PASS
