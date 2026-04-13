# 🔄 Nesne Hareketleri — Object Movement Animation

A simple **C# Windows Forms** application that animates a `PictureBox` moving in a continuous rectangular loop using four independent timers.

---

## 📋 About the Project

This project demonstrates how to control UI element movement in Windows Forms by chaining multiple `Timer` components. A `PictureBox` travels around the edges of the form in a clockwise rectangular path — up → right → down → left — and repeats indefinitely.

---

## 🚀 How It Works

The animation is driven by **4 timers**, each responsible for one direction of movement:

| Timer | Direction | Trigger Condition |
|-------|-----------|-------------------|
| `timer1` | ⬆️ Move Up | Stops when `Top <= 25`, starts `timer2` |
| `timer2` | ➡️ Move Right | Stops when `Left >= 750`, starts `timer3` |
| `timer3` | ⬇️ Move Down | Stops when `Top >= 425`, starts `timer4` |
| `timer4` | ⬅️ Move Left | Stops when `Left <= 55`, starts `timer1` |

Each timer moves the `PictureBox` by **5 pixels** per tick, creating a smooth looping animation.

---

## 🖥️ Technologies Used

- **Language:** C#
- **Framework:** .NET Windows Forms
- **IDE:** Visual Studio

---

## ⚙️ Setup & Run

1. Clone the repository:
   ```bash
   git clone https://github.com/yelda-batti0/Proje_Nesne_Hareketler.git
   ```
2. Open the solution file (`.sln`) in **Visual Studio**.
3. Build and run the project (`F5` or `Ctrl+F5`).

> ⚠️ This project targets **Windows** and requires the .NET Desktop Runtime.

---

## 📁 Project Structure

```
Proje_Nesne_Hareketler/
├── Form1.cs           # Main form logic and timer event handlers
├── Form1.Designer.cs  # Auto-generated UI layout
├── Program.cs         # Application entry point
└── ...
```

---

## 📌 Notes

- The boundary values (`25`, `750`, `425`, `55`) are matched to the default form size. If you resize the form, update these values accordingly.
- You can change the speed of the animation by modifying the timer `Interval` property in the designer or increasing/decreasing the step value (`5`).

---

## 📄 License

This project is open-source and available under the [MIT License](LICENSE).
