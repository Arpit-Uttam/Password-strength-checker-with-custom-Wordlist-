# Password Strength Analyzer & Wordlist Generator

A Python-based GUI tool to analyze password strength, detect breached passwords using a local dictionary, and generate custom wordlists for cybersecurity and ethical hacking purposes.

## Features

- Analyze password strength using zxcvbn
- Estimate crack time and guess count
- Check if password exists in a local breach dictionary (like rockyou.txt)
- Generate a custom wordlist from names, dates, or keywords
- GUI-based interface built with Tkinter
- Save wordlist to .txt file
- Offline support (no internet required)
- Exported as .exe using PyInstaller (optional)

## Technologies Used

- Python 3.x
- Tkinter for GUI
- zxcvbn for password strength analysis
- itertools for wordlist generation
- PyInstaller for Windows executable packaging

## How It Works

1. User enters a password into the GUI.
2. The password is analyzed using zxcvbn to determine:
   - Strength score (0 to 4)
   - Number of guesses
   - Estimated crack time
   - Suggestions and warnings
3. The password is also checked against a local dictionary file (e.g., common_passwords.txt).
4. The result is displayed in a text box.
5. For wordlist generation, the user enters multiple input keywords (e.g., names, dates).
6. The script generates common permutations and variations.
7. Final results are saved in a .txt wordlist.

## Installation

1. Clone this repository:
   git clone https://github.com/yourusername/password-analyzer-tool.git

2. Install the required package:
   pip install zxcvbn

3. (Optional) To generate an executable:
   pip install pyinstaller
   pyinstaller --onefile --windowed --add-data "common_passwords.txt;." password_gui_tool.py

## Running the Tool

To run the tool using Python:

   python password_gui_tool.py

Make sure `common_passwords.txt` is in the same directory.

## Example Files

- password_gui_tool.py - Main GUI code
- common_passwords.txt - Local dictionary of breached passwords
- custom_wordlist.txt - Output generated wordlist

## Use Cases

- Cybersecurity education and practice
- Red team tools and password testing
- Ethical hacking wordlist generation
- Awareness training on strong password creation

## Future Scope

- Export report as PDF or CSV
- Real-time password strength meter
- Web-based version using Flask or React
- Integration with HaveIBeenPwned API
- Password hashing (MD5, SHA256)

## Author

Developed by Arpit Uttam

## License

This project is open source and available under the MIT License.
