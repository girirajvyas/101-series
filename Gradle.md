# Gradle



# Download
 - Versions:
   - https://gradle.org/releases/
 - Download the verison relevant for you
   - Example: https://gradle.org/next-steps/?version=6.8.3&format=all

# Installation

## Set Env variable
 - Add new env variable:
	- GRADLE_HOME
	  - Example value: C:\Softwares\gradle-6.8.3-all\gradle-6.8.3
	- Append above variable to the PATH variable
	  - %GRADLE_HOME%\bin

## Verify 
 - Type `gradle` to verify installation
 - Output will be like below
 ```bash
    C:\Users\Giriraj_Vyas>gradle
    
    Welcome to Gradle 6.8.3!
    
    Here are the highlights of this release:
     - Faster Kotlin DSL script compilation
     - Vendor selection for Java toolchains
     - Convenient execution of tasks in composite builds
     - Consistent dependency resolution
    
    For more details see https://docs.gradle.org/6.8.3/release-notes.html
    
    Starting a Gradle Daemon (subsequent builds will be faster)
    
    > Task :help
    
    Welcome to Gradle 6.8.3.
    
    To run a build, run gradle <task> ...
    
    To see a list of available tasks, run gradle tasks
    
    To see a list of command-line options, run gradle --help
    
    To see more detail about a task, run gradle help --task <task>
    
    For troubleshooting, visit https://help.gradle.org
    
    Deprecated Gradle features were used in this build, making it incompatible with Gradle 7.0.
    Use '--warning-mode all' to show the individual deprecation warnings.
    See https://docs.gradle.org/6.8.3/userguide/command_line_interface.html#sec:command_line_warnings
    
    BUILD SUCCESSFUL in 6s
    1 actionable task: 1 executed
    C:\Users\Giriraj_Vyas>
  ```

 
 




# References
 - https://spring.io/guides/gs/gradle/#scratch
 
