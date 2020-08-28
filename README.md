- [Software Engineering 1](#software-engineering-1)
  - [Java & Eclipse Tutorial](#java--eclipse-tutorial)
    - [Install Java](#install-java)
      - [Install Java on Windows](#install-java-on-windows)
      - [Install Java on MacOS](#install-java-on-macos)
      - [Install Java on Ubuntu Linux](#install-java-on-ubuntu-linux)
    - [Install Eclipse](#install-eclipse)
      - [Install Eclipse on Windows](#install-eclipse-on-windows)
      - [Install Eclipse on MacOS](#install-eclipse-on-macos)
      - [Install Eclipse on Ubuntu Linux](#install-eclipse-on-ubuntu-linux)
  - [Course 01](#course-01)
    - [Topics](#topics)
    - [Exercises](#exercises)
      - [Simple "Hello-Java-App"](#simple-hello-java-app)
      - [Hello World Eclipse tutorial](#hello-world-eclipse-tutorial)
      - [JavaFX graphical user interface app](#javafx-graphical-user-interface-app)
  - [Course 02](#course-02)
  - [Course 03](#course-03)
  - [Course 04](#course-04)

# Software Engineering 1

## Java & Eclipse Tutorial

### Install Java

#### Install Java on Windows

1. Open https://adoptopenjdk.net  in your browser
2. Download and run the adopt open JDK installation wizard
![01_download_adopt_openjdk](images/01_download_adopt_openjdk.png)

3. Click through the adopt open jdk wizard:  
![02_openjdk_installer_1](images/02_openjdk_installer_1.png)
![03_openjdk_installer_2](images/03_openjdk_installer_2.png)
![04_openjdk_installer_3](images/04_openjdk_installer_3.png)
![5_openjdk_installer_4](images/05_openjdk_installer_4.png)
![06_openjdk_installer_5](images/06_openjdk_installer_5.png)
![07_openjdk_installer_6](images/07_openjdk_installer_6.png)
![08_openjdk_installer_7](images/08_openjdk_installer_7.png)

3. Verify that java has been installed successfully by running the command `java -version` in your Windows command line interface:
![09_verify_java_1](images/09_verify_java_1.png)
![10_verify_java_2](images/10_verify_java_2.png)
![11_verify_java_3](images/11_verify_java_3.png)

#### Install Java on MacOS

1. Download Adopt openJDK version from: https://adoptopenjdk.net/

#### Install Java on Ubuntu Linux

1. Open a terminal with **CTRL + ALT + T**
2. Run the following command:

    ```bash
    sudo apt install default-jdk
    ```

### Install Eclipse

#### Install Eclipse on Windows

1. Download the Eclipse installer from [the official Eclipse website](https://www.eclipse.org/downloads/packages/installer) for Windows
![](images/12_download_eclipse_installer.png)
2. Run the Eclipse installer from your Windows Explorer:
![](images/13_run_eclipse_installer_1.png)
2. Click through the installer to install Eclipse:
![](images/14_run_eclipse_installer_2.png)
![](images/15_run_eclipse_installer_3.png)
![](images/16_run_eclipse_installer_4.png)
![](images/17_run_eclipse_installer_5.png)



#### Install Eclipse on MacOS

1. Download the Eclipse installer from [the official Eclipse website](https://www.eclipse.org/downloads/packages/installer) for MacOs
2. ...
3. ...

#### Install Eclipse on Ubuntu Linux

If you like you can also run the Eclipse installer wizard on Ubuntu linux from https://www.eclipse.org/downloads/packages/installer or if you want to have an auto-updating Eclipse that might be not always updated with the most up to date version you can use the Eclipse snap either from https://snapcraft.io/eclipse or from the terminal like so:

1. Open a terminal with **CTRL + ALT + T**
2. Run the following command:

    ```bash
    sudo snap install eclipse --classic --edge
    ```

## Course 01

### Topics

1. Create, compile and run a simple "Hello World" java application.
2. Create, compile and run a java application with a simple JavaFX graphical user interface with Eclipse.

### Exercises

#### Simple "Hello-Java-App"

1. Open a simple text editor (Windows Notepad, Ubuntu Gedit or MacOs TextEdit) enter the following code and save it as ```Hello.java``` to your desired location:
    ```java
    public class Hello {
        public static void main(String args[]) {
            System.out.println("Hello Java");
        }
    }
    ```
2. Open a command line interface (Windows: Windows-Key + R -> Type "Cmd.exe", press enter, Ubuntu: CTRL + SHIFT + T, MacOs: search for "Terminal") and navigate to the location where you saved your Java Code with:
    ```bash
    cd PATH_TO_YOU_FILE
    ```
3. Type ```javac Hello.java``` and press enter
4. Now the java code has been compiled to ```Hello.class``` which you can run from within your terminal with:
    ```java
    java Hello
    ```

#### Hello World Eclipse tutorial

1. Open Eclipse
2. Click on "Create a Hello World application"
    ![](images/19_eclipse_hello_world.png)
3. Follow the guide on the right side of your screen to create the Hello World application and run it.

#### JavaFX graphical user interface app

1. Create a new JavaFX Project and name your main Class ```App.java```
2. Insert the following code to create a window with a button that prints "Hello World" to the terminal when you click it:
    ```java
    public class App extends Application {

        @Override
        public void start(Stage stage) {

            BorderPane borderPane = new BorderPane();        

            String message = "Hello Java!";
            Button button = new Button("Say: " + message);
            button.setOnAction((event) -> {
                System.out.println(message);
            });

            borderPane.setCenter(button);
            
            Scene scene = new Scene(borderPane, 400, 400);
            stage.setScene(scene);
            stage.show();
        }

        public static void main(String[] args) {
            launch(args);
        }

    }
    ```
![javafx_hello_world](images/20_eclipse_javafx_hello_world.png)

## Course 02

## Course 03

## Course 04