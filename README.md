# Enterprise-Systems-Integration

Spring Boot - Hello World App
I am using VSCode, but the code should work just fine on any other IDE.

You should have Java installed (You need Java SDK) on your machine, if you do not, you need to install it.

To be sure that you have Java installed, type in the terminal, and if Java is installed, you’ll see the version/ Otherwise, you need to install Java.

$ Java -version
Installing Spring Boot – VSCode
If you want to install Spring Boon in VSCode, you need to install the following extensions:

Java Extension Pack;
Spring Boot Extension Pack;
Note: you can install extensions in VSCode by clicking on the extension icon on the left bar (can be opened by (Windows: Ctrl + Shift +X). Then, write the name of the extension you want to install.

After installing the extensions, you can create a Spring Boot project by following these steps:

1. Open command pallet in VSCode (Windows: Ctrl + Shift + P, Mac: Cmd + Shift + P).

2. In the textbox, start writing spring and “spring initializer create a maven project” should appear, chose it by pressing Enter.

3. Spring initializer: Specify Spring Boot Version -> chose the latest stable version (Should be on top of other versions, no Snapshot).

4. Spring initializer: Project Language -> Java

5. Spring initializer: Input Group id -> the default is "com.example", but change it to something that better fits your project.

6. Spring initializer: Input Artifact id -> the default is “demo”, again change it to something that better fits your project.

7. Spring initializer: Specify packaging type -> JAR

8. Spring initializer: Specify Java Version -> 11, 17, 19 or 21 should be fine. I am choosing 17.

9. Spring initializer: Chose dependencies -> you need to choose the following dependency: Spring Web.

10. After selecting the aforementioned dependency, you need to press enter, and you’ll be asked where you want to save your project.

11. Save your project in the GitHub repo you have created, you'll see a message asking you if you want to open the project.

To be sure that everything is ok, try to run the application, by clicking run above the main function.

The server will run on port 8080, you can check if it is working by typing http://localhost:8080/ in the address bar in your browser. If all is good, you should see the following:


Do not worry, it is running but we did not code it to do anything yet.

Creating a simple rest controller
Right-click on the main package. Then, create a new java class, and input the name of the class (e.g., testRestAPI).

The class will look like the following

public class testRestAPI {

}
Modify your code to look as follows:

@RestController
public class testRestAPI {
    @GetMapping("/esi")
    public String helloWorld(){
    return "Welcome to the ESI course!";
    }
}
@RestController and @GetMapping annotations will appear with a red line under each of them indicating an error. Hover over each one of them and if you chose “quick fix”, it will suggest you to "import org.springframework.web.bind.annotation.RestController"; for the first, and "import org.springframework.web.bind.annotation.RestController;" for the last. Choose them and they will be added to your code and the problem will be solved.

Now, save your code, stop your server, then, run it again. After that, visit http://localhost:8080/esi

Do not worry about the code, we will be covering it next week

12. Commit and push the changes in the created project to GitHub.
