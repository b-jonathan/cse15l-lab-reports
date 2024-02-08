# Part 1

## Failure Inducing Test
```
  @Test
  public void testReverseInPlaceWorks() {
    int[] input1 = { 3, 4, 5, 7, 6 };
    ArrayExamples.reverseInPlace(input1);
    assertArrayEquals(new int[] { 6, 7, 5, 4, 3 }, input1);
  }
```

## No Failure Induced Test
```
 @Test
  public void testReverseInPlaceFailure() {
    int[] input1 = { 3 };
    ArrayExamples.reverseInPlace(input1);
    assertArrayEquals(new int[] { 3 }, input1);
  }
```

## Symptom
![Symptoms](img/symptom.png)

## The Bug (Before vs After)

Before:
```
static void reverseInPlace(int[] arr) {
  for (int i = 0; i < arr.length; i += 1) {
    arr[i] = arr[arr.length - i - 1];
  }
}
```

After:
```
static void reverseInPlace(int[] arr) {
  for (int i = 0; i < arr.length / 2; i += 1) {
    int temp = arr[i];
    arr[i] = arr[arr.length - i - 1];
    arr[arr.length - i - 1] = temp;
  }
}
```

Explanation:

The reason why the code before did not work is because it attempted to reverse the list by looping through the entire array. This doesnt work because after the halfway point, the array would be replacing the data at the index with itself because the data in the first half of the list was already replaced.


# Part 2 (grep options)

## grep -r



## grep -l



## grep -c



## grep -m --max-count=NUM


