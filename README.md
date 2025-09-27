# Wi-Fi Password Attempt Script (macOS)
## Overview

#### This script:

- Lists nearby Wi-Fi networks using macOS’s airport command.

- Reads candidate passwords from a password.csv file.

- Generates simple variants of each password (all caps, all lowercase, alternating case, etc.).

- Tries to connect to each nearby network with each password until one succeeds.

- Prints the successful network name, SSID, and password, then exits.



## Requirements

**macOS only (uses airport and networksetup).**

- Python 3 installed.

- A file named **password.csv** in the same directory as the script.

Format: each line should have at least one column, with the password in the first column.
Example:

```bash
password123
qwerty
letmein
```

## How to Run

- Save the script in a .py file (e.g., wifi_brute_crack.py).

- Put your password.csv in the same folder.

- Open Terminal and run:

```bash
python3 wifi_attempt.py
```

## Notes

- password.csv must not be empty, otherwise the script won’t try anything.

- Each password is expanded into 5 variants (lowercase, uppercase, first letter capitalized, alternating lower/upper).

- It may take several seconds per attempt since Wi-Fi handshakes are slow.
