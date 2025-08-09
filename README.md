# Please Read Before Using it
**Facebook Cookie Extractor**

This script automates the process of logging into multiple user accounts using a list of credentials, and retrieves session data (cookies) for each account.

**Intended strictly for testing and educational purposes only.**

## Features

- Supports batch processing of multiple accounts
- Automatic retries if failed
- Skips accounts that have been previously processed to avoid duplicates
- Automatically detects and saves cookies in the user’s **Download/CookiesExtractor/** folder, compatible with Android (Termux), Windows, Linux, and macOS
- Includes animated loading spinners and colored terminal output for better user experience
- Automatically delays 60 seconds after every 3 accounts to reduce checkpoint risk on Facebook
- Clean and readable terminal interface with banner and instructions
- Robust error handling with status messages: OK, checkpoint (CP), error
- Cross-platform support with smart download folder detection
- Easy to use with simple input format and clear instructions

## Dependencies

Before running the script on Termux (Android), install required packages:

```bash
pkg update && pkg upgrade
```
```
pkg install git python
```
```
Then install required Python packages:
```
```
pip install -r requirements.txt
```

How to Install

1. Clone the repository:


```
git clone https://github.com/berlianoel/cookiesids
```
```
cd cookiesids
```

2. Install dependencies:
```
pip install -r requirements.txt
```

3. Run the script:
```
python main.py
```

## Usage Instructions

Termux Android Users Only: Setup Storage Permissions

To allow saving files to your device storage, run this once before using the script:
```
termux-setup-storage
```
Grant the requested storage permission in the popup.


**Input Format**

You can enter accounts when prompted with the following format:
```
uid1|password1
uid2|password2
uid3|password3
```
**Example:**
```
600012325678901|mypassword123
600098765432109|examplepass321
```
When entering manually, input one account per line. After entering all accounts, press Enter twice to start the process.


## Output Location

The script will save extracted cookies to:

**<Download Folder>/CookiesExtractor/cookies.txt**

On **Termux** Android, this usually maps to:

/storage/emulated/0/Download/CookiesExtractor/cookies.txt

On Windows:

C:\Users\<YourUsername>\Downloads\CookiesExtractor\cookies.txt

On Linux/macOS:

/home/<YourUsername>/Downloads/CookiesExtractor/cookies.txt


The script tries to detect the correct download folder automatically.

## Important Notes

Make sure to run ```termux-setup-storage``` and grant storage permission before using this script on Termux Android.

The script will retry failed login attempts 3 times per account before skipping.

There will be a 60-second delay after processing every 3 accounts to reduce risk of Facebook checkpoint.

Duplicate accounts already processed (found in cookies.txt) will be skipped.

## Credits

Author: Berlin

please keep the author credit.

**The author is NOT responsible for any misuse or damages caused.**


## Warning

This project is for **educational** and testing purposes only.

**Do NOT** use it for illegal or unethical activities.


## Bug Reports & Issues

If you find bugs or have issues, please open a report in the GitHub Issues section of the repository.


Tools for Accessing Files

Android: ZArchiver or similar file manager apps. [Recommeded!](https://sfile.mobi/bA40eZ1Lag7)

Windows: File Explorer

Linux/macOS: File Manager or Terminal


**Thank you for using this script!**

