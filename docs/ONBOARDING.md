# Logisim-evolution Onboarding

Welcome to the Logisim-evolution development team! This document is designed to help you get up to speed with the project's codebase, key design decisions, and contribution guidelines.

## Project Overview

Logisim-evolution is an educational software for designing and simulating digital logic circuits. It is a free, open-source, and cross-platform application written in Java.

### Key Features:

*   **Circuit Designer:** An easy-to-use interface for creating and editing digital logic circuits.
*   **Simulation:** Real-time simulation of circuits to observe their behavior.
*   **Chronogram:** A tool to visualize the evolution of signals in your circuit over time.
*   **Hardware Integration:** Schematics can be simulated on real electronic boards.
*   **VHDL Components:** The behavior of components can be specified using VHDL.
*   **TCL/TK Console:** An interface for interaction between the circuit and the user.
*   **Extensive Component Library:** A vast collection of components, including LEDs, TTLs, switches, and SoCs.
*   **Custom Libraries:** The ability to load custom libraries on startup.
*   **Multi-language Support:** The application is available in multiple languages.

## Getting Started

This section will guide you through setting up your development environment, building the project from source, and running the application.

### Prerequisites

*   **Java Development Kit (JDK) 21 or newer:** Logisim-evolution is a Java application. You can download a suitable JDK from [Adoptium](https://adoptium.net/temurin/releases/).
*   **Git:** To clone the repository.

### Building and Running

1.  **Clone the repository:**
    ```bash
    git clone https://github.com/logisim-evolution/logisim-evolution.git
    cd logisim-evolution
    ```

2.  **Build the project:**
    The project uses Gradle for building. The included Gradle wrapper (`gradlew`) takes care of downloading the correct Gradle version. To build the project, run:
    ```bash
    ./gradlew build
    ```
    This command compiles the source code, runs tests, and creates a JAR file in the `build/libs` directory.

3.  **Run the application:**
    To run the application directly from the source, use the `run` task:
    ```bash
    ./gradlew run
    ```
    This will start the Logisim-evolution graphical user interface.

## Codebase Structure

The codebase is organized into the following main directories:

*   `src/main/java`: Contains the application's Java source code.
*   `src/main/resources`: Contains resource files, such as images and localization bundles.
*   `src/test`: Contains the source code for unit tests.

### Key Packages

The core logic of the application resides in the `com.cburch.logisim` package. Here's a breakdown of the most important sub-packages:

*   `com.cburch.logisim.circuit`: Core classes for representing and simulating circuits.
*   `com.cburch.logisim.comp`: Base classes for creating new circuit components.
*   `com.cburch.logisim.gui`: User interface components, including the main window, circuit editor, and dialogs.
*   `com.cburch.logisim.file`: Classes for loading, saving, and managing circuit files.
*   `com.cburch.logisim.proj`: High-level classes for managing projects.
*   `com.cburch.logisim.std`: The standard library of built-in components.
*   `com.cburch.logisim.tools`: Tools for interacting with the circuit editor, such as the wiring tool and the selection tool.

## Key Design Decisions

The architecture of Logisim-evolution is guided by the following principles:

*   **Separation of Concerns:** The codebase follows a pattern similar to Model-View-Controller (MVC), where the core logic of circuit simulation (`com.cburch.logisim.circuit`) is decoupled from the graphical user interface (`com.cburch.logisim.gui`). This separation makes the code easier to maintain and test.
*   **Component-Based Architecture:** The application is built around a system of reusable and extensible components. The `com.cburch.logisim.comp` package provides base classes that make it easy to create new components with custom behavior and appearance.
*   **Extensibility:** The design allows for the addition of new component libraries. This is a key feature that enables the community to extend the functionality of the software.
*   **Standard Java Desktop Application:** The user interface is built using Java's Swing toolkit. This ensures cross-platform compatibility.

## How to Contribute

We welcome contributions from the community! Here's how you can get involved:

*   **Reporting Bugs and Requesting Features:** If you find a bug or have an idea for a new feature, please [create an issue](https://github.com/logisim-evolution/logisim-evolution/issues) on our GitHub repository.
*   **Contributing Code:** If you'd like to contribute code, please follow these steps:
    1.  Fork the repository on GitHub.
    2.  Create a new branch for your changes.
    3.  Make your changes and commit them with clear and descriptive messages.
    4.  Push your changes to your fork.
    5.  Create a pull request against the `main` branch of the main repository.

For more detailed information, please see the [developer's documentation](../README.md#how-to-contribute).
