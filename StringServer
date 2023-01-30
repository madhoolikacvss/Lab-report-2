#Lab Report 2

**TASK 1** 

When I created StringServer.java, I borrowed the ideas from NumberServer.java and modified the methods used there to suit String data type.

![My Code](https://github.com/madhoolikacvss/Lab-report-2/blob/main/code.jpg)


My main method from the class StringServer takes in an argument (the server number) given by a user from VSCode's terminal and uses Server.java to create a local server.
For example, I used the command `java StringServer 55100` where 55100 is the server number. It is important for the argument being passing in the terminal of the IDE is stringctly integer, and within the range 1024 to 49151 as the server numbers are restricted to this range.
The result of the execution of the above code was as follows:
![Launching the server](https://github.com/madhoolikacvss/Lab-report-2/blob/main/serverstart.jpg)


Then, I added the path to the url of the server, `/add-message?s=helooo`, which gave the following output
![First line](https://github.com/madhoolikacvss/Lab-report-2/blob/main/add1.jpg)

My code uses the method `handleRequest(URI url)` from the class Handler to read the path in the url and detect the query which is the relevant value for this method - heloo.
Here, as it was first time running the server, there were no preadded strings to be displayed, so the first line of the output is *helooo*

I then added changed the path to the url of the server to `/add-message?s=skidooosh`, which gave the following output
![Second line](https://github.com/madhoolikacvss/Lab-report-2/blob/main/add2.jpg)

Here, as I already ran the server with a path previously, the method `handleRequest(URI url)` already had the string `helooo` stored in the variable `sentence`. 
So when this url was run, the new parameter (skidooosh) was concatinated to the variable `sentence` with an escape character `\n` which also added a new line before the word.
Later on, I also ran the code again with integers and doubles as parameters for a query, and the server displayed those numbers correctly. 
This because the numbers when being concatinated to the variable `sentence` in my method `handleRequest(URI url)` typecasted them into Strings. 


**TASK 2** 
I chose the algorith that was designed to take in an array and outpout a new array with the reverse the order of the elements.
Code with the issue in it.
```
static void reverseInPlace(int[] arr) {
    for(int i = 0; i < arr.length; i += 1) {
      arr[i] = arr[arr.length - i - 1];
    }
}
```

Initially, a test was run on the code above with one element in the array being reversed. 
```
@Test 
	public void testReverseInPlace() {
    int[] input1 = { 3 };
    ArrayExamples.reverseInPlace(input1);
    assertArrayEquals(new int[]{ 3 }, input1);
	}
  ```
Because there was only one elemtn in the array to begin with, we did not know if the program was running correctly - the reversed/unreversed versions will be the same.

The I made another test multiple elements in it causing the code's bugs to be revealed.
```
@Test 
	public void testReverseInPlace2() {
    int[] input1 = { 1,2,3, };
    ArrayExamples.reverseInPlace(input1);
    assertArrayEquals(new int[]{ 3,2,1 }, input1);
	}
```
Here, because the array had multiple elements in it, the mistake in the algorithm was visible. As shown below, the last element has replaced the first element's position which is correct. 
However, it also appears in its original position which is a sysptom of the bug.
![Issue](https://github.com/madhoolikacvss/Lab-report-2/blob/main/withIssue.jpg)

In the code, the last line in the for loop changes the original order of the array which erases the original elements present in the array. 
To fix this issue I made a dummy array with the same length of the orginal array. I then run a for loop that copies the elemtns of the original array into the new array in the reverse order!

Code after being fixed
```
static void reverseInPlace(int[] arr) {
    int[] newArr = reversed(arr);
    for(int i = 0; i < arr.length; i += 1) {
     arr[i] = newArr[i];
    }
}
```

#Task 3

In lab 2 I realised the importance of small logical errors in the code that potentially ruin the whole code. It is important to look at each step with great detail as some of the logical issues might not be obvious for human eyes unless through testing is done.
That leads me onto the second lesson - effective testing. Some testers might pass due to the nature of the inputs even though the code has errors. It is our responsibility to make testers that encompass a good number of possible input types to see if the algorithm works correctly at all times.





