<h1 align="center">Hash-Breaker</h1>

__What Is This?__ - Allows you to crack hashes with or without wordlist.

__How to Download__: Open the terminal on your machine and type the following command:

```bash
$ git clone https://github.com/KafetzisThomas/Hash-Breaker.git
```

Use [pip](https://pip.pypa.io/en/stable) to install the required packages:

```bash
$ pip install -r requirements.txt
```

## Features

* Supported hash algorithms: `Bcrypt`, `MD5`, `SHA1`, `SHA224`, `SHA256`, `SHA384`, `SHA512`
* Dynamic password generation: Generate all possible combinations of characters until a match is found
* Dictionary support
* Command-Line Arguments

## Usage Notes

To use the script, follow these steps in your terminal:

```bash
# Windows
python main.py

# Linux/Mac
chmod +x main.py
./main.py
```

# Command-Line Arguments

## Example 1: Cracking a hash with a wordlist:

```bash

➜ hash_to_crack='$2b$12$.pdcdWnjEA/2GOvHfEfMkupP/BXSsdJjLs5Sh63E0B/5JG/YeB9cu'  # Example Bcrypt hash
➜ wordlist_file=common_passwords.txt  # Path to wordlist file

# Using Hash-Breaker with a wordlist
$ python main.py bcrypt "$hash_to_crack" "$wordlist_path" --with-wordlist

# Output:
# ...
# Password Found: [ a ]
# Time elapsed: 3.1s
```

## Example 2: Cracking a hash with dynamic password generation:

```bash
➜ hash_to_crack='e1608f75c5d7813f3d4031cb30bfb786507d98137538ff8e128a6ff74e84e643'  # Example SHA256 hash

# Using Hash-Breaker with dynamic password generation
$ python main.py sha256 "$hash_to_crack"

# Output:
# ...
# Password Found: [ tom ]
# Time elapsed: 0.5s
```

## Example 3: Using different hash algorithms:

```bash
➜ sha512_hash =  # Replace with an example SHA512 hash
➜ sha1_hash =  # Replace with an example SHA1 hash
➜ md5_hash =  # Replace with an example MD5 hash

# Cracking a SHA512 hash
$ python main.py sha512 "$sha512_hash" "$wordlist_file" --with-wordlist 

# Cracking a SHA1 hash
$ python main.py sha1 "$sha1_hash" 

# Cracking a MD5 hash
$ python main.py md5 "$md5_hash" "$wordlist_file" --with-wordlist 
```

# Run Tests

```bash
➜ cd path/to/script/directory
$ python -m unittest discover tests
```

# Disclaimer: Educational Use Only

**Hash-Breaker** is an educational tool designed for `learning` and `understanding cryptographic concepts` related to hash functions and password security. It is NOT intended for malicious activities, unauthorized access, or any form of unethical use.

By accessing and using Hash-Breaker, you acknowledge and agree to the terms outlined in this disclaimer. **The repository owner and contributors are not responsible for any misuse, damage, or legal consequences resulting from the use of this tool.**

Please use Hash-Breaker responsibly and for **educational purposes only**.
