# Lab Report 2 – Servers and Bugs



**🌟Part 1: Simeplest Search Engine from week 2**
Here is the code for Search Engine
```
import java.io.IOException;
import java.net.URI;

class Handler implements URLHandler {
    // The one bit of state on the server: a number that will be manipulated by
    // various requests.
    String str = "";

    /* (non-Javadoc)
     * @see URLHandler#handleRequest(java.net.URI)
     */
    /* (non-Javadoc)
     * @see URLHandler#handleRequest(java.net.URI)
     */
    public String handleRequest(URI url) {
        if (url.getPath().equals("/")) {
            return String.format("String: %s", str);
        } 
        else if (url.getPath().contains("/search")) {
            String[] parameters = url.getQuery().split("=");
            String[] subStr = str.split(" ");
            String targetStr = "";
            for (int i = 0; i < subStr.length; i++){
                if (subStr[i].contains(parameters[1]))
                    targetStr = targetStr + " " + subStr[i];
            }
            return targetStr;
        } else {
            System.out.println("Path: " + url.getPath());
            if (url.getPath().contains("/add")) {
                String[] parameters = url.getQuery().split("=");
                if (parameters[0].equals("s")) {
                    str = str + " " + parameters[1];
                    return String.format("String added by %s! It's now %s", parameters[1], str);    
                }
            }
            return "404 Not Found!";
        }
    }
}

class SearchEngine {
    public static void main(String[] args) throws IOException {
        if(args.length == 0){
            System.out.println("Missing port number! Try any number between 1024 to 49151");
            return;
        }

        int port = Integer.parseInt(args[0]);

        Server.start(port, new Handler());
    }
}

```

I called add method to add pineapple to the string. In the original string, the string was empty, and after adding pineapple, the string now become pineapple.
![image](ScreenShotLab2-1.png)

I called add method again to add apple to the string. In the original string, the string was pineapple, and after adding apple, the string now become pineapple apple.
![image](ScreenShotLab2-2.png)

I called search method to search a substring app. The string is pineapple apple, and after searching app, pineapple and apple were diplaied because they have the substring app.
![image](ScreenShotLab2-3.png)


**🌟Part 2: Bugs**

*Array Methods

![image](ScreenShotLab2-4.png)
![image](ScreenShotLab2-5.png)
![image](ScreenShotLab2-6.png)
![image](ScreenShotLab2-8.png)
![image](ScreenShotLab2-7.png)


The test failed because of the AssertionError, which is because of the expected value different from the return value.

There are two bugs:

reverseInPlace: Only the first half of the array is reverse with the expected value, and the rest of the array stay the same.

reversed:  It creates a new array to store the reversed array, but it lets the old array copy the new array’s value which has nothing on it yet.












