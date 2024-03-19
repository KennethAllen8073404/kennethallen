# Kennethallen

A Node.js module for cryptographic tools and utilities.

## Installation

You can install this module via npm: `npm install kennethallen`

## Usage
```javascript
const cryptoToolsKit = require('crypto-tools-kit');

// Generate a random password
const randomPassword = cryptoToolsKit.generateRandomPassword();
console.log('Random Password:', randomPassword);

// Hash data
const data = 'sensitiveData';
cryptoToolsKit.hashData(data)
    .then(hash => console.log('Hash:', hash))
    .catch(error => console.error('Error:', error));

// Compare hash
const hashedData = '$2b$10$qoECbB6lCf.0vNX7LfbOhefz8p9q5fAx7F4Dl8qHMO8VTv62GAVqi';
cryptoToolsKit.compareHash(data, hashedData)
    .then(result => console.log('Comparison Result:', result))
    .catch(error => console.error('Error:', error));

// Encrypt data
const plainText = 'Hello, world!';
const key = 'supersecretkey';
const encryptedData = cryptoToolsKit.encryptData(plainText, key);
console.log('Encrypted Data:', encryptedData);

// Decrypt data
const decryptedData = cryptoToolsKit.decryptData(encryptedData, key);
console.log('Decrypted Data:', decryptedData);

// Generate RSA key pair
const { publicKey, privateKey } = cryptoToolsKit.generateKeyPair();
console.log('Public Key:', publicKey);
console.log('Private Key:', privateKey);
```

