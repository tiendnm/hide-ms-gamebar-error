
# Hide "Get an app to open ms-gamebar link"

This repository provides a simple solution to suppress the error **"Get an app to open ms-gamebar link"** and **"Get an app to open ms-gamingoverlay link"** on Windows. Instead of fixing the root cause, this solution hides the error entirely by redirecting the `ms-gamebar` and `ms-gamingoverlay` protocol to a silent script.

---

## 🚀 How It Works
The solution consists of two files:
1. **`disable-gamebar.reg`**: A registry file that adds support for the `ms-gamebar` and `ms-gamingoverlay` protocol and redirects it to a script.
2. **`gamebar.vbs`**: A VBScript that runs silently and executes a simple command without showing a console window.

---

## 🛠️ Installation Guide
### Step 1: Download the files
- Download the files [`disable-gamebar.reg`](disable-gamebar.reg) and [`gamebar.vbs`](gamebar.vbs) from this repository.

### Step 2: Edit the VBScript path (if needed)
If you save `gamebar.vbs` to a custom location, update the `disable-gamebar.reg` file to reflect the correct path:
```reg
@="wscript \"C:\\your\\custom\\path\\gamebar.vbs\""
```

### Step 3: Apply the registry fix
1. Double-click on the `disable-gamebar.reg` file.
2. When prompted, confirm adding the registry entries.

### Step 4: Test the solution
1. Open the **Run** dialog (`Win + R`).
2. Type `ms-gamebar:` and press **Enter**.
3. Open the **Run** dialog (`Win + R`).
4. Type `ms-gamingoverlay:` and press **Enter**.
5. If successful, you'll see no error, and the script will run silently.

---

## 🧩 Additional Information
### What does the fix do?
- Adds registry keys for the `ms-gamebar` protocol.
- Adds registry keys for the `ms-gamingoverlay` protocol.
- Redirects protocol handling to a silent script (`gamebar.vbs`).
- Prevents the "Get an app to open this link" error from appearing.

### Is it safe?
Yes, this fix is safe. It does not interfere with any system files or applications. However, always review `.reg` and `.vbs` files before applying them.

---

## 📝 License
This project is open-source and distributed under the [MIT License](LICENSE). Feel free to contribute and improve this solution for the community!

---

## 🌟 Support
If this solution helped you, give the repo a ⭐ and share it with others facing the same issue!
