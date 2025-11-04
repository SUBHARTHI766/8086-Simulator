# ⚙️ 8086 Web Simulator

![8086 Web Simulator Screenshot](https://via.placeholder.com/800x400?text=8086+Web+Simulator+Screenshot)


A simple, educational web-based simulator for the Intel 8086 microprocessor, designed to visualize how assembly code interacts with CPU registers and memory. This project is built using HTML, CSS, and JavaScript, providing a real-time, interactive learning experience directly in the browser.

**Developed by:**
-   **Subharthi Bose (RA2411003010105)**
-   **Aniruddha Dutta (RA2411003010087)**

---

## 🎯 Project Goal

The primary goal of this simulator is to demystify the core concepts of computer architecture by providing a visual, hands-on environment for learning 8086 assembly language. Users can write simple assembly programs and immediately see their impact on the CPU's registers and memory.

---

## ✨ Features

-   **Interactive Editor:** Write 8086 assembly code directly in the browser.
-   **Real-time Register Display:** Monitor the state of key 16-bit registers (AX, BX, CX, DX, FLAGS) in hexadecimal format.
-   **Memory Visualization:** Observe changes in a simulated memory block, showing modified addresses and their values.
-   **Execution Log:** Get step-by-step feedback on instruction execution in the output panel.
-   **Basic Instruction Set:** Supports fundamental data movement and arithmetic operations.
-   **Zero Flag Implementation:** Demonstrates how the `FLAGS` register is updated based on arithmetic results (specifically, the Zero Flag).
-   **"Cyber-Glow" UI:** A clean, console-like aesthetic for a focused learning experience.

---

## 🚀 How to Use

1.  **Open in Browser:**
    Simply open the `index.html` file in your preferred web browser. No server-side setup is required.

2.  **Write Code:**
    Enter your 8086 assembly instructions in the "Editor" textarea.

    **Example Code:**
    ```assembly
    ; Test all basic 8086 operations
    MOV AX, 5      ; AX = 5
    MOV BX, 10     ; BX = 10
    MOV CX, 2      ; CX = 2

    ADD AX, BX     ; AX = AX + BX (5 + 10 = 15)
    SUB AX, CX     ; AX = AX - CX (15 - 2 = 13)

    MOV MEM[20], AX ; Store AX (13) into Memory location 20
    MOV DX, MEM[20] ; Load Memory location 20 (13) into DX

    ADD DX, 7      ; DX = DX + 7 (13 + 7 = 20)
    SUB DX, AX     ; DX = DX - AX (20 - 13 = 7)

    MOV MEM[30], DX ; Store DX (7) into Memory location 30
    MOV AX, MEM[30] ; Load Memory location 30 (7) into AX
    ```

3.  **Run Simulation:**
    Click the **"Run"** button to execute your code. Observe the changes in the Registers, Memory, and Output panels.

4.  **Reset State:**
    Click the **"Reset"** button to clear all register values and memory, returning the simulator to its initial state.

---

## 📖 Implemented 8086 Instructions

The simulator currently supports a basic set of 8086 instructions:

-   **`MOV destination, source`**: Moves data from the source to the destination.
    -   `MOV Register, ImmediateValue` (e.g., `MOV AX, 123`)
    -   `MOV Register, Register` (e.g., `MOV AX, BX`)
    -   `MOV MEM[Address], Register` (e.g., `MOV MEM[100], AX`)
    -   `MOV Register, MEM[Address]` (e.g., `MOV AX, MEM[20]`)
-   **`ADD destination, source`**: Adds the source value to the destination register.
    -   `ADD Register, ImmediateValue` (e.g., `ADD AX, 5`)
    -   `ADD Register, Register` (e.g., `ADD AX, BX`)
    -   `ADD Register, MEM[Address]` (e.g., `ADD AX, MEM[20]`)
-   **`SUB destination, source`**: Subtracts the source value from the destination register.
    -   `SUB Register, ImmediateValue` (e.g., `SUB AX, 5`)
    -   `SUB Register, Register` (e.g., `SUB AX, BX`)
    -   `SUB Register, MEM[Address]` (e.g., `SUB AX, MEM[20]`)

---

## 🚩 FLAGS Register (Simplified)

The `FLAGS` register is a 16-bit register that stores status and control flags. In this simulator, we've implemented a simplified version focusing on the **Zero Flag (ZF)**.

-   **Zero Flag (ZF):**
    -   Set to `0x0040` (binary `0100 0000`) if the result of an `ADD` or `SUB` operation is exactly **zero**.
    -   Set to `0x0000` otherwise.
    This demonstrates how the CPU tracks conditions essential for conditional branching.

---

## 🏗️ Project Structure

-   `index.html`: The main HTML file containing the simulator's structure and UI.
-   `style.css` (or inline `<style>`): Defines the visual styling of the simulator, including the "Cyber-Glow" theme.
-   `script.js` (or inline `<script>`): Contains the core JavaScript logic for the 8086 emulator, handling instruction parsing, register updates, memory management, and UI interactions.

---

## 📜 License

This project is for educational purposes only.

---

**Made with ❤️ for learning Computer Architecture.**
