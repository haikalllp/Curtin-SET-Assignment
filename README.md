# SET Assignment - Sudoku Algorithm
Forked from [TheAlgorithms/Java](]https://github.com/TheAlgorithms/Java)

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

### 1. Windows (Command Prompt)

1. Open a **Command Prompt** and `cd` into the project root (where `gradlew.bat` resides).

2. **Compile & run the Sudoku solver**

```cmd
   gradlew.bat run
```

This will compile the code (if needed) and launch the `com.thealgorithms.puzzlesandgames.Sudoku` main class, printing the solved puzzle to the console.

3. **Run all tests**

   ```cmd
   gradlew.bat test
   ```

   Executes JUnit 5 tests for `Sudoku`.

4. **Compile only (no run/tests)**

   ```cmd
   gradlew.bat assemble
   ```

   Produces compiled classes and JAR under `build/` without executing them.

5. **Run a single test class**

   ```cmd
   gradlew.bat test --tests "com.thealgorithms.puzzlesandgames.SudokuTest"
   ```

   Replace the FQCN in quotes to target any other test.

---

### 2. Windows (PowerShell)

PowerShell does not automatically look in the current directory for `.bat` scripts. Prefix with `.\`:

1. In your project root, run:

   ```powershell
   .\gradlew.bat run
   .\gradlew.bat test
   .\gradlew.bat assemble
   ```
2. To target a single test:

   ```powershell
   .\gradlew.bat test --tests "com.thealgorithms.puzzlesandgames.WordBoggleTest"
   ```

---

### 3. Linux / macOS (bash, zsh, etc.)

1. **Make the wrapper executable** (one-time):

   ```bash
   chmod +x gradlew
   ```

2. **Compile & run the Sudoku solver**

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

## Importing into an IDE

Most modern Java IDEs (IntelliJ IDEA, Eclipse, VS Code) can import a Gradle project:

1. **Open** your IDE’s “Import Project” or “Open” dialog.
2. **Select** the root folder of this repo.
3. **Choose** “Import as Gradle project” (or equivalent).
4. The IDE will download dependencies, set up the Java 17 toolchain, and configure run/test configurations automatically.

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