# Servers and Bugs
## Part 1: String Server
```
# String Server Web
import java.io.IOException;
import java.net.URI;

class Handler implements URLHandler {
    // The one bit of state on the server: a number that will be manipulated by
    // various requests.

    String str = new String("");

    public String handleRequest(URI url) {
        if (url.getPath().equals("/")) {

            return String.format("Welcome to the String Server! \n" +
            "Please use the path /add-message?s=[string] to add a new string.");

        } else {
            System.out.println("Path: " + url.getPath());

            if (url.getPath().contains("/add-message")) {
                String[] parameters = url.getQuery().split("=");

                if (parameters[0].equals("s")) {

                    str = str + parameters[1] + "\n";
                    return str;
                }
            }
            return "404 Not Found!";
        }
    }
}

class StringServer {
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
Before any string is added, the web server looks like this.\
![Before](Before.png)


After adding one string, this is what the web server looked like.\
![One String](OneString.png)


After adding another string, this is what the web server looked like.\
![Multiple String](MultipleStrings.png)


The URLHandler method is called in both cases and the relevant argument is the URL. It changes what is returned as well as the URL. As mentioned above, we have added a `\n` character which places the cursor in the next line. Since the next line has no data, the string that we input gets stored in that line and the cursor again moves to the next line. This is why the contents in the previous line remain as they were. 


## Part 2: One bug from Lab 3
The bug that I have chosen is from ArrayExamples.java. The method reversedInPlace is supposed to change the input array to be in reversed order.\
But the method doesn't correctly do what it is supposed to. It reverses the elements, but as it reaches the middle of the array the loop starts
using the new reversed values to switch elements. \
The JUnit test I wrote with a failure inducing input is as follows:
```
# JUnit test with failuring inducing input
@Test
  public void testReverseInPlace2(){
    int[] input = {1,2,3,4,5};
    ArrayExamples.reverseInPlace(input);
    assertArrayEquals(new int[] {5,4,3,2,1}, input);
  }
```
This does not give us the desired output. The output this prints is {5,4,3,4,5}.


The JUnit test runs perfectly fine without making any chances to the code of `reversedInPlace` if the input is different.\
One such input that *does not* induce a failure is as follows:
```
# JUnit test without failure inducing input
@Test 
	public void testReverseInPlace() {
    int[] input1 = { 3 };
    ArrayExamples.reverseInPlace(input1);
    assertArrayEquals(new int[]{ 3 }, input1);
	}
```
This gives us the desired output. But that does not mean the code is fixed.


The following messages are displyed while running the above mentioned tests.\
The test `testReversedInPlace()` passes. The green tick on the left-hand side indicates the same.\
![Successful](Passing_Test.png)


The test `testReversedInPlace2()` fails. The expected value and actual value do not match.\
![Failing](https://github.com/hetvi1511/cse15l-lab-reports/blob/main/Failure_Inducing_Input.png)


The bug in `reversedInPlace` is, it reverses the elements but after reaching halfway through the array the for loop starts using the new reversed values
to switch the elements in the array. To fix this code, we need to change the condition in the for loop that does the switching.


The `reverseInPlace` code before making the changes, so that it runs properly is as follows:
```
# Original code which does not give the desired output for all possible inputs.
static void reverseInPlace(int[] arr) {
    for(int i = 0; i < arr.length; i += 1) {
      arr[i] = arr[arr.length - i - 1];
    }
  }
```


The `reverseInPlace` code after making the changes, so that it runs properly is as follows:
```
# Edited code which works properly for all possible inputs.
static void reverseInPlace(int[] arr) {
    for(int i = 0; i < arr.length/2; i += 1) {
      int temp = arr[i];
      arr[i] = arr[arr.length - i - 1];
      arr[arr.length - i - 1] = temp;
    }
  }
```


By making the following changes, we go from 0th index to the index at the middle of the array. For each, we switch with the last element.


## Part 3: New Learnings from Lab 2 and Lab 3
In lab 2, we learned the following things:
- Cloning a repository with GitHub Desktop.
- Learning about the `URLHandler` Interface, and building and running a simple server.
- Running the same server on a remote server by applying what we learnt in Lab 1.
- Making a simple "Search Engine" which can add new strings and search and display the list of strings.


In lab 3, we learned the following things:
- Finding and fixing bugs found in the various codes given to us.
- Writing different tests to determine if the code is working as it should with different inputs.
