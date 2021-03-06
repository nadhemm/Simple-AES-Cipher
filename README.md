# Simple-AES-Cipher
[![Build Status](https://travis-ci.org/teitei-tk/Simple-AES-Cipher.svg?branch=master)](https://travis-ci.org/teitei-tk/Simple-AES-Cipher)

Pycrypto based very simple AES cipher client

### Dependencies
* Python 2.7 or later
* Pycrypto 2.6.1 or later

### Install
```bash
$ pip install Simple-AES-Cipher
```

### Usage
```python
from simple_aes_cipher import AESCipher, generate_secret_key

pass_phrase = "hogefuga"
secret_key = generate_secret_key(pass_phrase)

# generate cipher
cipher = AESCipher(secret_key)

raw_text = "abcdefg"
encrypt_text = cipher.encrypt(raw_text)
assert raw_text != encrypt_text

decrypt_text = cipher.decrypt(encrypt_text)
assert encrypt_text != decrypt_text
assert decrypt_text == raw_text
```

## Contributing
Bug reports and pull requests are welcome on GitHub at https://github.com/teitei-tk/Simple-AES-Cipher.

## LICENSE
* MIT
