# 📇 Contact Management System

A simple and practical Command-Line Interface (CLI) application for managing contacts using Python. This project allows users to add new contacts, view the contact list, and search for contacts by phone number.

## 📋 Table of Contents

- [Features](#-features)
- [Architecture](#️-architecture)
- [Technologies Used](#️-technologies-used)
- [Installation](#-installation)
- [Usage](#-usage)
- [Project Structure](#-project-structure)
- [Main Functions](#-main-functions)
- [Testing](#-testing)
- [Contributing](#-contributing)
- [License](#-license)

---

## ✨ Features

### Core Functionalities

- 📇 **Add Contact:** Collects contact information including first name, last name, phone number, and title.
- 🚫 **Duplicate Prevention:** Checks phone numbers to prevent adding duplicate contacts.
- 📋 **View Contact List:** Displays all saved contacts with their information in a formatted output.
- 🔍 **Search by Phone Number:** Finds a contact using their phone number.
- 🚪 **Exit Program:** Safely terminates the application.

### User Interface

- 💻 **Command-Line Interface (CLI):** Provides a simple and readable text-based menu.
- ⚠️ **Error Handling:** Displays appropriate messages for duplicate contacts, contacts not found, and invalid menu options.

---

## 🏗️ Architecture

This project follows the **Separation of Concerns** principle to keep the code organized, readable, and maintainable.

```text
┌─────────────────────┐
│      main.py        │
│   User Interface    │
└──────────┬──────────┘
           │
           ↓
┌─────────────────────┐
│ contact_module.py   │
│   Business Logic    │
└──────────┬──────────┘
           │
           ↓
┌─────────────────────┐
│    Contact List     │
│   Storage Layer     │
└─────────────────────┘
```

### Architecture Layers

- **User Interface Layer:** Handles the menu and user interactions.
- **Business Logic Layer:** Manages contact information, prevents duplicates, and performs search operations.
- **Storage Layer:** Stores contact information in an in-memory Python list.

---

## 🛠️ Technologies Used

- **Language:** Python 3.10+
- **Data Structure:** Python Lists and Dictionaries.
- **Libraries:** Only built-in Python features are used. No external packages are required.
- **Testing:** `contact_test.py` is included for testing the project.

---

## 📦 Installation

### Prerequisites

- Python 3.10 or higher
- Git

### Setup Steps

**1. Clone the repository:**

```bash
git clone YOUR_GITHUB_REPOSITORY_URL
```

**2. Navigate to the project directory:**

```bash
cd Contact_Management_System
```

**3. Run the application:**

```bash
python main.py
```

No external dependencies are required.

---

## 🚀 Usage

After running the application, the main menu will appear:

```text
1) Add contact
2) Contact list
3) Search contact by phone
0) Exit

Enter a option:
```

### Main Operations

- **Option 1 (Add Contact):** Collects the first name, last name, phone number, and title. It also checks whether the phone number already exists.
- **Option 2 (Contact List):** Displays all saved contacts with their information.
- **Option 3 (Search):** Searches for a contact using the entered phone number and displays the matching contact if found.
- **Option 0 (Exit):** Closes the application.

---

## 📁 Project Structure

```text
Contact_Management_System/
│
├── main.py                 # Main entry point (menu and main loop)
├── contact_module.py       # Contact management functions
├── contact_test.py         # Test file
│
└── README.md               # Project documentation
```

---

## 📚 Main Functions

### contact_module.py

This file contains the main business logic of the application:

- **contact_list:** A global list that stores contact information as dictionaries.
- **show_menu():** Displays the main menu and gets the user's choice.
- **get_contact_info():** Collects contact information and returns it as a dictionary.
- **print_contact_list(contact_list):** Displays all contacts with formatted output using f-strings.
- **find_contact_by_phone(contact_list, phone):** Searches for a contact by phone number and returns the matching contact if found.

### main.py

This file handles the main application flow:

- Uses a `while` loop to keep the application running.
- Uses `match-case` statements to handle user menu selections.
- Connects the user interface to the contact management functions.

---

## 🧪 Testing

The project includes a separate test file named `contact_test.py`.

To run the test file, execute:

```bash
python contact_test.py
```

---

## 👥 Contributing

Contributions and suggestions for improving this project are welcome.

If you would like to contribute:

1. Fork the repository.
2. Create a new branch:

```bash
git checkout -b feature/AmazingFeature
```

3. Commit your changes:

```bash
git commit -m "Add some AmazingFeature"
```

4. Push your branch:

```bash
git push origin feature/AmazingFeature
```

5. Open a Pull Request.

### Code Style

- Follow the PEP 8 style guide.
- Use descriptive and readable names for variables and functions.
- Keep the code clean and organized.

---

## 📄 License

No license has been specified yet.

---

**Made with ❤️ by Nazanin Montazeri**