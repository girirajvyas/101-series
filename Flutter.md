# Setup

## Download Flutter + Dart
 - https://docs.flutter.dev/get-started/install
 - update the downloaded path to PATH variable in env variable
 - once done, run in:
   - CMD: `where flutter dart`
   - powershell: `where.exe flutter dart`
 - Output:
   ```cmd
   C:\Users\Giriraj_Vyas>where flutter dart
   C:\Softwares\flutter_windows_3.3.9-stable\flutter\bin\flutter
   C:\Softwares\flutter_windows_3.3.9-stable\flutter\bin\flutter.bat
   C:\Softwares\flutter_windows_3.3.9-stable\flutter\bin\dart
   C:\Softwares\flutter_windows_3.3.9-stable\flutter\bin\dart.bat
   ```

## Verify installation
 - Run: `flutter doctor`
 - Output:
  ```cmd
  Running "flutter pub get" in flutter_tools...                      15.7s
  Doctor summary (to see all details, run flutter doctor -v):
  [√] Flutter (Channel stable, 3.3.9, on Microsoft Windows [Version 10.0.19044.2251], locale en-IN)
  [X] Android toolchain - develop for Android devices
      X Unable to locate Android SDK.
        Install Android Studio from: https://developer.android.com/studio/index.html
        On first launch it will assist you in installing the Android SDK components.
        (or visit https://flutter.dev/docs/get-started/install/windows#android-setup for detailed instructions).
        If the Android SDK has been installed to a custom location, please use
        `flutter config --android-sdk` to update to that location.
  
  [√] Chrome - develop for the web
  [X] Visual Studio - develop for Windows
      X Visual Studio not installed; this is necessary for Windows development.
        Download at https://visualstudio.microsoft.com/downloads/.
        Please install the "Desktop development with C++" workload, including all of its default components
  [!] Android Studio (not installed)
  [√] Connected device (3 available)
  [√] HTTP Host Availability
  
  ! Doctor found issues in 3 categories.
  ```


## Install + Setup Android Studio
 - https://docs.flutter.dev/get-started/editor?tab=androidstudio
   - Download from: https://developer.android.com/studio
   - Install
 - Run: `flutter doctor`
 - Output:
   ```cmd
   Running "flutter pub get" in flutter_tools...                      15.7s
   Doctor summary (to see all details, run flutter doctor -v):
   [√] Flutter (Channel stable, 3.3.9, on Microsoft Windows [Version 10.0.19044.2251], locale en-IN)
   [X] Android toolchain - develop for Android devices
       X Unable to locate Android SDK.
         Install Android Studio from: https://developer.android.com/studio/index.html
         On first launch it will assist you in installing the Android SDK components.
         (or visit https://flutter.dev/docs/get-started/install/windows#android-setup for detailed instructions).
         If the Android SDK has been installed to a custom location, please use
         `flutter config --android-sdk` to update to that location.
   
   [√] Chrome - develop for the web
   [X] Visual Studio - develop for Windows
       X Visual Studio not installed; this is necessary for Windows development.
         Download at https://visualstudio.microsoft.com/downloads/.
         Please install the "Desktop development with C++" workload, including all of its default components
   [√] Android Studio (version 2021.3)
   [√] Connected device (3 available)
   [√] HTTP Host Availability
   
   ! Doctor found issues in 3 categories.
   
   ```
 - Go to Android Studio -> Tools -> SDK Manager -> ANdroid SDK -> SDK Tools Tab 
   - Tick "Android SDK Command Line Tools (latest)" -> Apply -> it will download the depenedencies
 - Run: `flutter doctor`
 - Output:
   ```cmd
   C:\Users\Giriraj_Vyas>flutter doctor
   Doctor summary (to see all details, run flutter doctor -v):
   [√] Flutter (Channel stable, 3.3.9, on Microsoft Windows [Version 10.0.19044.2251], locale en-IN)
   [!] Android toolchain - develop for Android devices (Android SDK version 33.0.1)
       ! Some Android licenses not accepted.  To resolve this, run: flutter doctor --android-licenses
   [√] Chrome - develop for the web
   [X] Visual Studio - develop for Windows
       X Visual Studio not installed; this is necessary for Windows development.
         Download at https://visualstudio.microsoft.com/downloads/.
         Please install the "Desktop development with C++" workload, including all of its default components
   [√] Android Studio (version 2021.3)
   [√] Connected device (3 available)
   [√] HTTP Host Availability
   
   ! Doctor found issues in 2 categories.
   ```
 - if you see above their is a command mentioned, we need to run it to install the android licenses:
 - Command: `flutter doctor --android-licenses`
 - Multiple times we have to accept via typing 'y' and then finally you will get below output
 - Output: 
   ```cmd
   ---------------------------------------
   Accept? (y/N): y
   All SDK package licenses accepted
   ```
 - You will have 1 issue then as below which can be ignored
   ```
   C:\Users\Giriraj_Vyas>flutter doctor
   Doctor summary (to see all details, run flutter doctor -v):
   [√] Flutter (Channel stable, 3.3.9, on Microsoft Windows [Version 10.0.19044.2251], locale en-IN)
   [√] Android toolchain - develop for Android devices (Android SDK version 33.0.1)
   [√] Chrome - develop for the web
   [X] Visual Studio - develop for Windows
       X Visual Studio not installed; this is necessary for Windows development.
         Download at https://visualstudio.microsoft.com/downloads/.
         Please install the "Desktop development with C++" workload, including all of its default components
   [√] Android Studio (version 2021.3)
   [√] Connected device (3 available)
   [√] HTTP Host Availability
   
   ! Doctor found issues in 1 category.
   ```

### Setup Emulator
 - Now You need to decide where you want to run your app:
 - So for android you need emulator to run your app as an android app
 - Create the same via Android Studio
   - Device manager (Right hand side)
   - Delete if already one is created as it will give you error while running
   - Error message is:
   - ```
     PS C:\Workspaces\vscode\flutter_application_1> flutter emulators --launch Pixel_3a_API_33_x86_64
     PS C:\Workspaces\vscode\flutter_application_1>
     PS C:\Workspaces\vscode\flutter_application_1>
     PS C:\Workspaces\vscode\flutter_application_1>
     PS C:\Workspaces\vscode\flutter_application_1>
     PS C:\Workspaces\vscode\flutter_application_1>
     The Android emulator exited with code 1 during startup
     Android emulator stderr:
     WARNING | Failed to process .ini file C:\Users\Giriraj_Vyas\.android\avd\Pixel_3a_API_33_x86_64.avd\quickbootChoice.ini for    
     reading.
     ERROR   | x86_64 emulation currently requires hardware acceleration!
     CPU acceleration status: HAXM is not installed on this machine
     More info on configuring VM acceleration on Windows:
     https://developer.android.com/studio/run/emulator-acceleration#vm-windows
     General information on acceleration: https://developer.android.com/studio/run/emulator-acceleration.
   ```
   - Create emulator:
     - Select a system image: selected "R" (it will take some time to download around 1.1 GB)
	 - Enable hardware HXM with default 4GB settings
 - Done


## VSCode setup
 - Open Command Pallete(CTRL+SHIFT+P) -> `Extensions: Install Extensions`
 - Install extensions: Flutter and Dart
 - In terminal run: `flutter run`
 - Output:
   ```cmd
   PS C:\Workspaces\vscode\flutter_application_1> flutter run
   Using hardware rendering with device sdk gphone x86. If you notice graphics artifacts, consider enabling software rendering
   with "--enable-software-rendering".
   Launching lib\main.dart on sdk gphone x86 in debug mode...
   Checking the license for package Android SDK Tools in C:\Users\Giriraj_Vyas\AppData\Local\Android\sdk\licenses
   License for package Android SDK Tools accepted.
   Preparing "Install Android SDK Tools (revision: 26.1.1)".
   "Install Android SDK Tools (revision: 26.1.1)" ready.
   Installing Android SDK Tools in C:\Users\Giriraj_Vyas\AppData\Local\Android\sdk\tools
   "Install Android SDK Tools (revision: 26.1.1)" complete.
   "Install Android SDK Tools (revision: 26.1.1)" finished.
   Checking the license for package Android SDK Build-Tools 30.0.3 in C:\Users\Giriraj_Vyas\AppData\Local\Android\sdk\licenses    
   License for package Android SDK Build-Tools 30.0.3 accepted.
   Preparing "Install Android SDK Build-Tools 30.0.3 (revision: 30.0.3)".
   "Install Android SDK Build-Tools 30.0.3 (revision: 30.0.3)" ready.
   Installing Android SDK Build-Tools 30.0.3 in C:\Users\Giriraj_Vyas\AppData\Local\Android\sdk\build-tools\30.0.3
   "Install Android SDK Build-Tools 30.0.3 (revision: 30.0.3)" complete.
   "Install Android SDK Build-Tools 30.0.3 (revision: 30.0.3)" finished.
   Checking the license for package Android SDK Platform 31 in C:\Users\Giriraj_Vyas\AppData\Local\Android\sdk\licenses
   License for package Android SDK Platform 31 accepted.
   Preparing "Install Android SDK Platform 31 (revision: 1)".
   "Install Android SDK Platform 31 (revision: 1)" ready.
   Installing Android SDK Platform 31 in C:\Users\Giriraj_Vyas\AppData\Local\Android\sdk\platforms\android-31
   "Install Android SDK Platform 31 (revision: 1)" complete.
   "Install Android SDK Platform 31 (revision: 1)" finished.
   Running Gradle task 'assembleDebug'...                            527.4s
   √  Built build\app\outputs\flutter-apk\app-debug.apk.
   Installing build\app\outputs\flutter-apk\app.apk...              1,759ms
   Syncing files to device sdk gphone x86...                          113ms
   
   Flutter run key commands.
   r Hot reload.
   R Hot restart.
   h List all available interactive commands.
   d Detach (terminate "flutter run" but leave application running).
   c Clear the screen
   q Quit (terminate the application on the device).
   
    Running with sound null safety 
   
   An Observatory debugger and profiler on sdk gphone x86 is available at: http://127.0.0.1:61201/fw2Ap6LGFrU=/
   The Flutter DevTools debugger and profiler on sdk gphone x86 is available at:
   http://127.0.0.1:9101?uri=http://127.0.0.1:61201/fw2Ap6LGFrU=/
   ```
 - You will have flutter dummy app created with clicking on + icon will increase the count

## Commands:
 - Flutter sdk path: C:\Softwares\flutter_windows_3.3.9-stable\flutter\bin\cache\dart-sdk
 - flutter emulators
 - flutter emulators --launch Pixel_6_Pro_API_33_6_GB
 - Flutter emulators --launch Pixel_3a_API_33_x86_64
 - flutter emulators --launch Pixel_2_API_30
 - flutter run
 - flutter build apk

## Flutter run key commands.
r Hot reload. 
R Hot restart.
h List all available interactive commands.
d Detach (terminate "flutter run" but leave application running).
c Clear the screen
q Quit (terminate the application on the device).

