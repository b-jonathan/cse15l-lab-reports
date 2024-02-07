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
