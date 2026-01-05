# PDF Viewer

**PDF Viewer** is an Android application developed for an educational institution that allows users to **navigate through a hierarchical folder structure** and **securely view multiple PDF documents** within the app.

The application enforces **read-only access**, preventing file downloads or external sharing, and ensuring controlled access to educational materials.

---

## Features

- Hierarchical navigation based on a JSON-defined structure
- Secure, in-app PDF viewing (read-only)
- No file download or external opening permissions
- Text search within PDF documents
- Automatic viewer timeout after inactivity

---

## Installation & Setup

1. **Install the APK**
   - You can scan the APK on VirusTotal (the app is safe and free of malware).

2. **Prepare the PDF files**
   - Create a folder named `ArchivosPdf` in:
     ```
     /storage/emulated/0/
     ```
   - Place all PDF files inside this folder.

3. **Create the JSON structure file**
   - Create a JSON file that defines the navigation structure.
   - An example file is available in the `files` folder.

### JSON Structure

Each element in the JSON file supports the following keys:

- **`type`**  
  Defines the button behavior:
  - `curso`: Acts as a folder (navigation level)
  - `documento`: Opens the assigned PDF file

- **`nombre`**  
  Display name of the button

- **`descripcion`**  
  - For `curso`: Text displayed at the top of the screen  
  - For `documento`: Name of the PDF file (including `.pdf`)

- **`subelementos`**  
  List of child elements, following the same structure

---

## Usage

1. Open the application (**Android 13 or higher required**).
2. On first launch, select the JSON file to load the navigation structure. (You can change it later on the settings icon on top-right corner. The password is "iescierva")
3. Navigate through the buttons generated from the JSON.
4. Open and read PDF documents directly within the app.
5. Use the built-in search to find text inside PDFs.
<img width="540" height="1200" alt="image" src="https://github.com/user-attachments/assets/661e782f-3a6c-49a6-a4bd-7ad69133360b" />
<img width="509" height="840" alt="image" src="https://github.com/user-attachments/assets/e9f0e08a-a017-4cd9-a98a-f456ac0092c9" />



---

## Security & Access Control

- PDFs can only be viewed inside the application.
- Downloading, sharing, or opening files with external apps is not allowed.
- The PDF viewer automatically closes after **2 minutes of inactivity**, returning the app to its initial state for the next user.

---

## License

This project was developed for educational purposes.
