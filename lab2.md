# Part 1
## StringServer Code

The following code is the contents of StringServer.java

![Image](lab2-images/lab2-1.1.jpg)

## /add-message usage
### Screenshot 1

![Image](lab2-images/lab2-1.2.jpg)

- The method that is called in this code would be the `handleRequest` method.

- In this method the relevant argument would be the url that we have typed. Along with this the method has relevant values. Two of the main values that are created as the method is called are the String arraylist `text`, which is used to hold the strings inputted, and the integer `len`, which is used to hold the value of the length of `text`. Since it is the first time calling the function, the value of `text` will be an empty arraylist and the value of `len` will equal 0. Since `url.getPath().equals("/")` is false the function goes into the else statement and since `url.getPath().equals("/add-message")` is true, the fucntion creates the empty String variable `response` and the String array `parameters` that hold the value of the query split by the `=` sign.

- If the first value of the query or `parameters[0]` is equal to the string value `"s"`, then the text present in `parameters[1]` is added to the the arraylist `text`, then the value of `len` is incremented by 1. After this, the value of `response` is updated with the values of `text` and their respective index.
