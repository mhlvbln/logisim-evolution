# Logisim-evolution Onboarding

Welcome to the Logisim-evolution project! This document will help you get up to speed with the codebase.

## Project Structure

The project is organized as follows:

- \`build.gradle.kts\`: This is the main build file for the project. It defines the project's dependencies, plugins, and build tasks.
- \`settings.gradle.kts\`: This file configures the project's settings, including the project name.
- \`src/\`: This directory contains all the source code for the project.
  - \`src/main/java/\`: The main application code.
  - \`src/main/resources/\`: The application's resources, such as images and configuration files.
  - \`src/test/java/\`: The test code.
- \`docs/\`: This directory contains the project's documentation.
- \`gradle/\`: This directory contains the Gradle wrapper, which allows you to build the project without installing Gradle.
- \`support/\`: This directory contains support files for creating distributable packages.
- \`ONBOARDING.md\`: This file! It's your guide to getting started with the project.
- \`README.md\`: The main README file for the project. It provides a high-level overview of the project and links to more detailed documentation.

## Build Process

To build the project, you can use the Gradle wrapper included in the repository.

1. **Build the project:**
   ```bash
   ./gradlew build
   ```
2. **Run the application:**
   ```bash
   ./gradlew run
   ```
3. **Create distributable packages:**
   ```bash
   ./gradlew createAll
   ```
   This will create packages for your current operating system (e.g., `.deb` for Linux, `.msi` for Windows, `.dmg` for macOS).

## Code Organization

The code is organized into the following main packages:

- \`com.cburch.logisim.circuit\`: This package contains the core logic for simulating digital logic circuits.
- \`com.cburch.logisim.comp\`: This package contains the components that can be placed on the circuit, such as gates, flip-flops, and multiplexers.
- \`com.cburch.logisim.gui\`: This package contains the graphical user interface for the application.
- \`com.cburch.logisim.file\`: This package contains the code for loading and saving circuit files.
- \`com.cburch.logisim.proj\`: This package contains the code for managing projects, which can contain multiple circuits.
- \`com.cburch.logisim.tools\`: This package contains the tools for interacting with the circuit, such as the wiring tool and the selection tool.

## Key Design Decisions

- **Java Swing for the UI:** The application is built using Java Swing, a mature and cross-platform GUI toolkit. This allows the application to run on a wide variety of operating systems.
- **Modular Design:** The codebase is organized into distinct packages, each with a specific responsibility. This separation of concerns makes the code easier to understand, maintain, and extend.
- **Event-Driven Architecture:** As a Swing application, Logisim-evolution is event-driven. User interactions with the GUI trigger events that are handled by the application's code.
- **Core Simulation Engine:** The \`com.cburch.logisim.circuit\` package contains the core simulation engine, which is responsible for simulating the behavior of digital logic circuits. This engine is the heart of the application.
