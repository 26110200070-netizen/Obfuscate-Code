# 🛠️ Universal Payload Encoder & Obfuscator V3.0

> **Admin & Developer:** Khoa Dev 👑

---

## 📘 Overview
**Universal Obfuscator V3.0** is a powerful security tool written in Python, designed to encode and obfuscate source code across three popular languages: **Python (.py)**, **Lua/Luau (.lua)**, and **JavaScript (.js)**. 

The tool protects intellectual property and prevents reverse engineering (decompilation) or unauthorized code inspection by transforming the original source into a complex, chaotic structure while fully preserving its original runtime functionality.

---

## 🚀 Capabilities (What Admin Khoa Dev Can Do)

With Admin privileges and the integrated feature set, Khoa Dev can perform the following operations:

* **Dynamic Multi-Language UI (i18n):** Seamlessly switch the console interface between English (`en`) and Vietnamese (`vi`) upon startup.
* **Multi-Platform Target Support:** Quickly obfuscate script payloads written in Python, Lua, or JavaScript.
* **Flexible Source Input Methods:** * Load existing script files (`.py`, `.lua`, `.js`) directly from the local computer.
    * Paste source code directly into the terminal console, finalizing the input easily by typing `END` on a new line.
* **Automated Output Generation:** Automatically export the obfuscated result with the correct corresponding file extension, calculating the precise payload size (in bytes) post-processing.

---

## ⚙️ How the Engine Works

The obfuscation system operates through a combination of a **Shift Cipher (Key-based encryption)**, **Junk Code Injection**, and **Polymorphic Identifier Mutation**:

### 1. Polymorphic Stub Generation
The system utilizes the `generate_confusing_name()` function to generate random variable identifiers consisting strictly of visually confusing characters: `I`, `l`, `O`, `0`, and `_`. The resulting variables are extremely difficult to distinguish with the naked eye (e.g., `lII_O0_l`, `O_0_IlI`).

### 2. Junk Code Injection
Before and after the core execution logic, the engine automatically injects 2 to 5 lines of meaningless code that complies with the target language's syntax. This disrupts static analysis tools and decompilers.

### 3. Language-Specific Obfuscation Engines:
* **Lua Target:** Characters are converted into their respective UTF-8 byte values and shifted by a randomized encryption key. At runtime, the script uses a decoder loop combined with `loadstring` or `load` to execute the payload directly in memory.
* **Python Target:** Utilizes a list comprehension to shift character ordinals (`ord()`), flattening the entire script into a compressed **One-liner** executed via the `exec()` function.
* **JavaScript Target:** Encrypts characters into an integer array, building a runtime decoder wrapper that compiles and triggers the payload via `new Function()`, compatible with both NodeJS and browser environments.

---

## 📦 System Requirements & Dependencies

The tool is highly optimized and runs entirely on Python's **built-in core libraries**, meaning **no external installations (such as `pip install ...`) are required**.

### Requirements:
* **Python:** Version 3.x or higher.
* **OS:** Fully compatible with Windows (CMD/PowerShell) and Linux/macOS (Terminal) utilizing standard ANSI color codes.

### Standard Libraries Used:
* `os`: Handles console clearing (`cls`/`clear`) and file path validation.
* `time`: Delays execution slightly to generate the UI loading animations.
* `random`: Generates randomized encryption keys, junk code density, and polymorphic variable strings.
* `string`: Pulls standard character sets to construct random junk values.
* `sys`: Controls standard output streams (`sys.stdout.write`) to render the dynamic progress loaders.

---

## 💻 Step-by-Step Usage Guide

1. **Launch the tool:**
   ```bash
   python obfuscateKhoaDev.py
