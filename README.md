# Password Generator

A Python script to generate secure and customizable passwords with configurable parameters for length, numerical digits, special characters, uppercase letters, and lowercase letters. This tool ensures that all constraints are satisfied, providing strong and secure passwords for your needs.

## Features

- **Customizable Length**: Specify the desired length of your password.
- **Enforce Constraints**: Ensure the inclusion of a minimum number of digits, special characters, uppercase letters, and lowercase letters.
- **Highly Secure**: Uses Python's `secrets` module for cryptographically strong random password generation.
- **Simple and Flexible**: Easy to use with sensible default values.

## How It Works

The script generates a random password by:

1. Defining possible character sets: letters, digits, and special symbols.
2. Creating a password of the specified length by randomly selecting characters from the combined pool.
3. Validating that the generated password meets the user-specified constraints.
4. Regenerating if constraints are not met until all conditions are satisfied.

## Installation

Clone this repository to your local machine:

```bash
git clone https://github.com/jorge-ross/password_generator.git
cd password-generator
```

## Usage

Run the script directly from the command line:

```bash
python generate_password.py
```

By default, the script generates a password with the following parameters:

- Length: 16 characters
- At least 1 digit
- At least 1 special character
- At least 1 uppercase letter
- At least 1 lowercase letter

### Custom Parameters

You can modify the function call in the script to customize the password generation. For example:

```python
new_password = generate_password(length=20, nums=2, special_chars=2, uppercase=3, lowercase=5)
```

This generates a 20-character password with at least:

- 2 digits
- 2 special characters
- 3 uppercase letters
- 5 lowercase letters

### Example Output

```
Generated password: x8@Pw2R1#^3w6A!Y
```

## Code Overview

### Function: `generate_password`

#### Parameters

- `length` (int): Total length of the password. Default is 16.
- `nums` (int): Minimum number of numerical digits. Default is 1.
- `special_chars` (int): Minimum number of special characters. Default is 1.
- `uppercase` (int): Minimum number of uppercase letters. Default is 1.
- `lowercase` (int): Minimum number of lowercase letters. Default is 1.

#### Returns

- `password` (str): A randomly generated password that satisfies all specified constraints.

## Dependencies

This script requires Python 3.6 or later. No additional libraries are needed.

## Contributing

Contributions are welcome! Feel free to submit issues or pull requests for new features, bug fixes, or improvements.

## License

This project is licensed under the MIT License. See the `LICENSE` file for details.

## Acknowledgments

This script was developed with simplicity and security in mind, leveraging Python's robust standard library.
