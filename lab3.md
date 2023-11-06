# Part 1 - Bugs
For this part of the lab I chose to do the following answers on the ArrayExamples.java file.

## Failure Inducing input for ArrayExamples.java reverseInPlace method
```
public class ArrayTests {
	@Test 
	public void testReverseInPlace() {
    int[] input1 = { 1, 2, 3, 4, 5, 6 };
    ArrayExamples.reverseInPlace(input1);
    assertArrayEquals(new int[]{ 6, 5, 4, 3, 2, 1 }, input1);
	}
}
```

## Input that doesn’t induce a failure for ArrayExamples.java reverseInPlace method
```
public class ArrayTests {
	@Test 
	public void testReverseInPlace() {
    int[] input1 = { 1 };
    ArrayExamples.reverseInPlace(input1);
    assertArrayEquals(new int[]{ 1 }, input1);
	}
}
```

## Symptoms of running the above tests
These were the tests ran:
![Image](lab3-images/lab3-1.1.JPG)

The follwoing was the result of running the above tests
![Image](lab3-images/lab3-1.2.JPG)

## Code changes to fix the bug in the method.
Code of the reverseInPlace method before:
```
static void reverseInPlace(int[] arr) {
  for(int i = 0; i < arr.length; i += 1) {
    arr[i] = arr[arr.length - i - 1];
  }
}
```

Code for reverseInPlace method after the fix:
```
static void reverseInPlace(int[] arr) {
  int temp = 0;
  for(int i = 0; i < arr.length/2; i += 1) {
    temp = arr[i];
    arr[i] = arr[arr.length - i - 1];
    arr[arr.length - i - 1] = temp;
  }
}
```


