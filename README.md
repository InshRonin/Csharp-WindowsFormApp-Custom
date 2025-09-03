# 🖼 Custom WinForms UI with Rounded Corners

This project is a **C# Windows Forms application** that demonstrates how to build a **custom window UI** without the default title bar.  
It uses **WinAPI (`dwmapi.dll`)** to apply modern rounded corners and provides custom buttons for minimizing, maximizing, and closing the window.

---

## 🚀 Features

- 🎨 **Rounded corners** using `DwmSetWindowAttribute`
- ⬆️ **Custom maximize / restore button**
- ➖ **Custom minimize button**
- ❌ **Custom exit button**
- 🖱 **Draggable form** (click and drag anywhere to move the window)
- 🔲 No default title bar — fully customizable design

---

## 🛠 Tech Stack

- **Language:** C#  
- **Framework:** .NET (Windows Forms)  
- **Interop:** Windows API (`dwmapi.dll`)  

---

---

## ⚙️ How It Works

- On startup, the app applies rounded corners:

```csharp
var attribute = DWMWINDOWATTRIBUTE.DWMWA_WINDOW_CORNER_PREFERENCE;
var preference = DWM_WINDOW_CORNER_PREFERENCE.DWMWCP_ROUND;
DwmSetWindowAttribute(this.Handle, attribute, ref preference, sizeof(uint));
````

* Buttons provide custom window control:

  * `button1` → Exit application
  * `button2` → Toggle maximize/restore
  * `button3` → Minimize and unfocus

* The **mouse down + move events** let the user drag the window from anywhere on the form.


## 🖥 Getting Started

1. Clone the repository:

   ```bash
   git clone https://github.com/InshRonin/Csharp-WindowsFormApp-Custom.git
   ```
2. Open the project in **Visual Studio**.
3. Build and run.

---

## 📌 Possible Extensions

* Add a **custom title bar** with icons.
* Implement **dark/light themes**.
* Integrate with **modern UI frameworks** (e.g., GunaUI, Siticone, Bunifu).

---

## 📝 License

This project is licensed under the **MIT License** — free to use and modify.

---

## 👨‍💻 Author

Developed by **Inshaf**

```
