# Password Manager

A secure and user-friendly password manager built with Python and Tkinter. This application helps you generate strong passwords, store them securely, and retrieve them when needed.

## Features

- 🔐 **Secure Password Generation**: Generate strong, random passwords with letters, numbers, and symbols
- 💾 **JSON Storage**: Store passwords securely in a structured JSON format
- 🔍 **Password Search**: Quickly find stored passwords by website name
- 📋 **Clipboard Integration**: Automatically copy generated passwords to clipboard
- 🎨 **User-Friendly GUI**: Clean and intuitive graphical interface
- ⚡ **Quick Entry**: Pre-filled email field for faster password creation

## Screenshots

The application features a clean, modern interface with:
- Website entry field
- Email/Username field (pre-filled)
- Password field with generation capability
- Search functionality
- Add button to save credentials

## Installation

### Prerequisites

- Python 3.6 or higher
- Poetry (recommended) or pip

### Using Poetry (Recommended)

1. Clone the repository:
```bash
git clone https://github.com/xtymac/password-manager_v2.git
cd password-manager_v2
```

2. Install dependencies:
```bash
poetry install
```

3. Run the application:
```bash
poetry run python main.py
```

### Using pip

1. Clone the repository:
```bash
git clone https://github.com/xtymac/password-manager_v2.git
cd password-manager_v2
```

2. Install required packages:
```bash
pip install pyperclip
```

3. Run the application:
```bash
python main.py
```

## Usage

### Adding a New Password

1. Enter the website name in the "Website" field
2. The email field is pre-filled, but you can modify it if needed
3. Click "Generate Password" to create a strong password (automatically copied to clipboard)
4. Click "Add" to save the credentials

### Searching for a Password

1. Enter the website name in the "Website" field
2. Click "Search" to find stored credentials
3. A popup will display the email and password for that website

### Password Generation

The password generator creates secure passwords with:
- 8-10 random letters (uppercase and lowercase)
- 2-4 random numbers
- 2-4 random symbols
- All characters are shuffled for maximum security

## File Structure

```
password-manager_v2/
├── main.py              # Main application file
├── logo.png             # Application logo
├── data.json            # Password storage (created automatically)
├── pyproject.toml       # Poetry configuration
├── poetry.lock          # Poetry lock file
└── README.md            # This file
```

## Data Storage

Passwords are stored in a `data.json` file with the following structure:

```json
{
  "example.com": {
    "email": "user@email.com",
    "password": "generated_password"
  }
}
```

## Security Notes

- Passwords are stored in plain text in the JSON file
- For production use, consider implementing encryption
- Keep your `data.json` file secure and backed up
- The application doesn't include network functionality, keeping your data local

## Dependencies

- `tkinter` - GUI framework (included with Python)
- `pyperclip` - Clipboard functionality
- `json` - JSON file handling (included with Python)
- `random` - Password generation (included with Python)

## Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## License

This project is open source and available under the [MIT License](LICENSE).

## Acknowledgments

- Built as part of "The Complete Python Pro Bootcamp" course
- Uses Tkinter for the graphical user interface
- Password generation inspired by security best practices

## Future Enhancements

- [ ] Password encryption
- [ ] Master password protection
- [ ] Import/Export functionality
- [ ] Password strength indicator
- [ ] Dark mode theme
- [ ] Backup and sync options 