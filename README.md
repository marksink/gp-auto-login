
# gp-auto-login

This script automates the login process for GlobalProtect VPN on macOS. It monitors clipboard content for credentials and handles interactions with the GlobalProtect application and OKTA Verify.

## Features

- Automatically handles VPN login via GlobalProtect.
- Supports decryption of passwords if necessary.
- Monitors clipboard for OKTA codes and pastes them into the correct input field.
- Ensures only one instance of the script is running at a time.

## Prerequisites

- Python 3.x
- Required Python packages: `pyautogui`, `pyperclip`, `psutil`
- OpenSSL for decryption if using encrypted passwords

## Installation

1. Clone this repository:
   ```sh
   git clone https://github.com/marksink/gp-auto-login.git
   cd gp-auto-login
   ```

2. Install the required Python packages:
   ```sh
   pip install pyautogui pyperclip psutil
   ```

3. Set up your environment:
   - Ensure that the GlobalProtect application is installed and configured on your macOS system.
   - Configure the script with your decryption passphrase and other settings as needed.

## Usage

1. **Run the Script:**
   You can run the script from the terminal:
   ```sh
   python global_protect_auto_login.py
   ```

2. **Configuration:**
   - Set `encryption_passphrase` to your passphrase for decrypting passwords.
   - Adjust `password_prefix` if your password prefix differs.
   - Modify `max_password_length` if your password or prefix is longer than 35 characters.

3. **Functionality:**
   - The script monitors the clipboard for passwords and OKTA codes.
   - It uses AppleScript to interact with GlobalProtect and the macOS UI.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Contributing

1. Fork the repository.
2. Create a new branch for your changes.
3. Commit your changes and push to the branch.
4. Create a pull request.

## Contact

For any questions or issues, please contact [your email address].
