# poc-app-android-automation
## Example of test automation in an Android app

To execute tests on the app (**Android-MyDemoAppRN.1.3.0.build-244.apk**) using **Robot Framework** and **Appium**, follow the steps below:

1. Make sure you have Robot Framework and Appium installed in your development environment.

2. Clone the project repository of the Android application using the following command:
    ```
    git clone https://github.com/dione-quevedo-avanade/poc-app-android-automation.git
    ```

3. Navigate to the project's root directory and open a terminal.

4. Install the project dependencies by running the following command:
    ```
    pip install -r requirements.txt
    ```

5. Start the Appium server by running the following command:
    ```
    npx appium
    ```

6. Identify the available emulators in your environment using the command:
    ```
    emulator -list-avds
    ```

7. Start the chosen emulator using the command:
    ```
    emulator -avd <avd_name>
    ```

8. Open a new terminal and navigate to the root directory of the test automation project.

9. Run the **`local`** tests using the following command:
    ```
    robot -d logs/local/ tests/*-local.robot
    ```

10. For _remote_ tests hosted on **`BrowserStack`**, use the following command:
    ```
    browserstack-sdk robot -d logs/browserstack/ tests/*browserstack.robot
    ```

This will execute all the tests present in the `tests/` directory using Robot Framework and Appium.

Make sure the avd device is online and the connection settings are correct in the Appium configuration file.
