# Encrypt-Share

## Abstract
This project develops a secure cloud storage application compatible with popular platforms like Dropbox, Box, Google Drive, and Office365. It encrypts uploaded files, allowing decryption only for members of a designated "Secure Cloud Storage Group." Implemented using Python, open-source cryptographic libraries, and Google Drive API, it features user authentication, user management, Google Drive API integration, menu generation, encryption/decryption, and a graphical user interface (GUI). Future enhancements may focus on hybrid key management and improved GUI security.

## Workflow
The project involves developing a private cloud space for securely uploading and downloading files. Users can be added or removed from this space, and files are encrypted before being uploaded to the cloud. Authentication is required to access the private space, and authorization (key) is needed to download files.

## Implementation
### User Management
The application initializes by checking for a key and registered users. It prompts for admin account creation if no users are registered, grants admin privileges for user management and key generation, and securely stores user credentials using pickling.

### Google Drive API Integration
The application interfaces with Google Drive API for file upload, download, and search. Functions like uploadFile() and downloadFile() handle encrypted file operations, while Encrypt() and Decrypt() ensure secure data handling.

### Menu Generation
The admin menu includes options for user management and key generation, while the standard menu provides file management options for regular users.

### Encryption/Decryption
Encryption and decryption use the Fernet encryption scheme from the cryptography library. Key generation and retrieval functions ensure secure handling of encryption keys.

### Authentication
Google Drive authentication follows the guidelines provided in the Google Drive API QuickStart guide, ensuring secure access to cloud storage resources.

### Graphical User Interface (GUI)
The application uses the Eel library for integrating Python backend functions with HTML, CSS, and JavaScript frontend components, providing an intuitive user interface.
