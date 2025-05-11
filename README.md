# SET Assignment - Sudoku Algorithm
Forked from [TheAlgorithms/Java](https://github.com/TheAlgorithms/Java)

## Setup JDK 17 (Windows)

1. Download and install JDK 17 from [JDK 17](https://adoptium.net/en-GB/temurin/releases/?version=17&package=jdk&os=any) (recommended).

2. Set the `JAVA_HOME` environment variable to point to the JDK installation directory.

```cmd
setx JAVA_HOME "C:\Program Files\Eclipse Adoptium\jdk-17.0.15.6-hotspot"
```
> Note : The path may vary based on your installation directory.

To find path:
```cmd
where java
```

3. Check if the `JAVA_HOME` variable is set correctly by running the following command in the command prompt:

> Note: You may need to restart computer for it to take effect.

```cmd
echo %JAVA_HOME%
```

4. Check if Java is installed correctly by running the following command:

```cmd
java --version
```

## How to run the code

### 1. Windows (PowerShell)

PowerShell does not automatically look in the current directory for `.bat` scripts. Prefix with `.\`:

1. In your project root, run:

   ```powershell
   # Run the program
   .\gradlew.bat run

   # Run all test
   .\gradlew.bat test

   # Compile only no run/test
   .\gradlew.bat assemble
   ```
2. To target a single test:

   ```powershell
   .\gradlew.bat test --tests "com.thealgorithms.puzzlesandgames.SudokuTest"
   ```

### 2. Windows (Command Prompt)

1. In your project root, run:

   ```cmd
   # Run the program
   gradlew.bat run

   # Run all test
   gradlew.bat test

   # Compile only no run/test
   gradlew.bat assemble
   ```
2. To target a single test:

   ```cmd
   gradlew.bat test --tests "com.thealgorithms.puzzlesandgames.SudokuTest"
   ```
   
---

### 3. Linux / macOS (bash, zsh, etc.)

1. **Make the wrapper executable** (one-time):

   ```bash
   chmod +x gradlew
   ```

2. **Compile & run the Sudoku.java**

   ```bash
   ./gradlew run
   ```

3. **Run all tests**

   ```bash
   ./gradlew test
   ```

4. **Compile only**

   ```bash
   ./gradlew assemble
   ```

5. **Run a single test class**

   ```bash
   ./gradlew test --tests "com.thealgorithms.puzzlesandgames.SudokuTest"
   ```

---

## Cleaning up

* To remove build artifacts:

  ```bash
  ./gradlew clean
  ```

## Project Structure

```
├── docs # Documentation files
│   └── Assignment-SET.pdf
├── gradle # Gradle wrapper files
├── .obsidian # All of obsidian configuration files
├── Excalidraw # All of our graphs
├── src
│   ├── main
│   │   └── java
│   │       └── com
│   │           └── thealgorithms
│   │               └── puzzlesandgames
│   │                   └── Sudoku.java # The methods we use
│   └── test
│       └── java
│           └── com
│               └── thealgorithms
│                   └── puzzlesandgames
│                       └── SudokuTest.java # The corresponding test cases
├── .gitignore
├── build.gradle
├── gradlew
├── gradlew.bat
└── README.md # Readme file
```

## Group members:
- **Adni Abdat** - 21545472
- **Ihsan Hasny** - 21483611
- **Haikal Putrayudha** - 21604483
