# Week 3 Lab Report - Servers and Bugs
**Daniel Sanei**

*This report describes the code for the web server I created, as well as analyzes one of the bugs encountered.*

## Part 1 - StringServer

Here is the code for the web server:

![lab3-1](https://user-images.githubusercontent.com/122568617/215354294-e0420bf2-71bf-484e-84b8-4c421ae066fb.JPG)

And here is the code in use, where the string "Hello" is displayed on the web server:

![5423534543](https://user-images.githubusercontent.com/122568617/215354723-c8a99ff4-3c1e-4c7e-819a-6f43fc3ce533.jpg)

Here, the only relevant method call is to handleRequest(URI url), whose argument contains the URI value for the url to the web server.
If given an appropriate class path within the url, then the code concatenates the string contained in the query (which is the second element of the parameters[] array), stores it into the allStr String variable, and displays it on the web server (which in this case, is the string "Hello"). Otherwise, it gives a "404 Not Found!" error message.

The second screenshot concatenates a second string:
(Note: the image displays several '%' characters within the URL, however, the query string was typed as 'How are you')

![4356334](https://user-images.githubusercontent.com/122568617/215354725-512c7b52-8f59-4d28-9cd2-756ac32a610a.jpg)

Like the first one, this request only calls the method handleRequest(URI url), with the same argument containing the web server's url.
Here, the string is "How are you", which is concatenated to the string from the first screenshot in the variable allStr.

## Part 2 - Analyzing a Bug
For the method reversed() in the provided code for this lab, I encountered a bug that caused the a failure during JUnit testing.
The failure-inducing input was the following:
```
@Test
public void testReversed()
{
  int[] input2 = {1,2,3,4,5};
  assertArrayEquals(new int[]{5,4,3,2,1}, ArrayExamples.reversed(input2);
}
```

In constrast, the following is an input that did not induce a failure during testing:
```
@Test
public void testReversed()
{
  int[] input1 = {};
  assertArrayEquals(new int[]{}, ArrayExamples.reversed(input1);
}
```

The symptom is as shown, with the first test passing successfully while the second fails:
![image](https://user-images.githubusercontent.com/122568617/215351296-3550a660-b11d-4d41-8047-2d716d3ffccb.png)

Before fixing the bug, the code was as shown:
```
  // Returns a *new* array with all the elements of the input array in reversed
  // order
  static int[] reversed(int[] arr) {
    int[] newArray = new int[arr.length];
    for(int i = 0; i < arr.length; i += 1) {
      arr[i] = newArray[arr.length - i - 1];
    }
    return arr;
  }
```

Here is the adjusted code that successfully passes both tests:
```
  // Returns a *new* array with all the elements of the input array in reversed
  // order
  static int[] reversed(int[] arr) {
    int[] newArray = new int[arr.length];
    for(int i = 0; i < arr.length / 2; i += 1) {
      int currentElement = arr[i];
      newArray[i] = arr[arr.length - i - 1];
      newArray[arr.length - i - 1] = currentElement;
    }
    if ( arr.length % 2 == 1 )
      newArray[arr.length/2] = arr[arr.length/2];
    return newArray;
  }
```

The fixes to the code were that the condition in the for loop was changed to half of the array length (rather than the full, which produced an incorrect result),
and in addition, the original array was storing the reversed elements of the newArray, which is the opposite of what was intended (the newArray should be assigned
the reversed elements of the original array). These 2 changes fixed the bug, and the code passes both of the previous tests successfully.

## Part 3 - Something New
I was aware that it was possible to run local and remote servers, but I've always wondered what the number (i.e. 4000) within the URL meant.
After this lab, I learned that the number represents the port number, and that it doesn't have to be any specific port for the server to run.
I also wondered why this port number only sometimes appears within a URL, but from the lab I now know that the browser on my computer usually
uses the default ports 80 or 443, and doesn't display them since they're the default ports.
