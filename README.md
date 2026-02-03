# Project README: Reflection-Based Class Analyzer with Swing Interface

This project implements a desktop application that uses the **Java Reflection API** to perform deep inspection of Java class files. It features both a command-line interface and a graphical user interface (GUI) to visualize class structures, including fields, constructors, methods, and implemented interfaces.

---

## 🛠 Project Components

The application is structured into two primary layers: a Command Line Interface (CLI) for class loading and a Swing-based Graphical User Interface (GUI) for data presentation.

### 1. Reflection CLI Layer (`ReflectionCLI.java`)

* **Dynamic Class Loading**: Utilizes `URLClassLoader` to load `.class` files from arbitrary file system paths.
* **Metadata Extraction**: Discovers and extracts detailed information about a class:
* **Fields**: Names and data types.
* **Constructors**: Parameter types and counts.
* **Methods**: Return types, names, and parameter strings.
* **Interfaces**: Names of all interfaces implemented by the target class.


* **Formatting**: Features a helper method `getParameterString` to convert parameter arrays into readable, comma-separated strings.

### 2. Swing UI Layer (`ObjectInspector.java`)

* **Visual Display**: Uses a `JTable` to present the reflected data in a clean, structured format.
* **Table Architecture**:
* Implements a custom `DefaultTableModel` with cell immutability to prevent user editing.
* Automatically categorizes data into sections (e.g., "Fields", "Methods") using descriptive header rows.


* **Dynamic Loading UI**: Users can select a class file via a file chooser, triggering the reflection analysis and populating the table in real-time.

---

## 🚀 How to Use

### Setup & Requirements

1. **JDK**: Ensure a Java Development Kit (JDK 8 or higher) is installed.
2. **Environment**: Create a project structure and ensure all classes are within the same directory or package for consistent execution.

### Running the CLI

1. **Command**: Execute the `ReflectionCLI` main method, passing the path to a `.class` file as a single argument.
2. **Output**: The terminal will display the discovered fields, constructors, methods, and interfaces for the specified class.

### Running the GUI

1. **Launch**: Execute the `ObjectInspector` class to open the graphical window.
2. **Analyze**:
* Click the "Load Class" (or similar) action to browse for a `.class` file.
* The application will load the class, perform the reflection analysis, and fill the table with the extracted metadata.



---

## 📂 File Manifest

* **`ReflectionCLI.java`**: Logic for class loading and reflection data extraction.
* **`ObjectInspector.java`**: Swing-based GUI for visualizing the class structure.
