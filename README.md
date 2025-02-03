# Project-4---GridKennel

### Objective:
In this lab, you will apply your existing `Dog` class to create and manage a **kennel system** using a **2D array**. The `GridKennel` class will store dogs in a structured way, allowing for adding, removing, filtering, and counting dogs by breed.

---

## Class: `GridKennel`

### Instance Variables:
- `numRows`: Number of rows in the kennel (integer).
- `numCols`: Number of columns in the kennel (integer).
- `kennel`: 2D array of `Dog` objects. Each element either stores a `Dog` object or `null` if the space is empty.

---

## Methods to Implement:

### 1. Constructor
```java
public GridKennel(int r, int c)
```

- Initializes an empty kennel with the given number of `rows` and `columns`.
- All spaces in kennel should start as `null`.

### 2.  Add a Dog
```java
public boolean addDog(Dog dog, int row, int col)
```

- <b>Prevents adding a dog outside of bounds</b> → Print "Error: Invalid kennel position." and return `false`.
- <b>Prevents overwriting an occupied space</b> → Print "Error: This kennel spot is already occupied." and return `false`.
- <b>Successfully adds a dog</b> → Place the Dog object in the array and return `true`.

### 3.  Remove a Dog
```java
public Dog removeDog(int row, int col)
```
- <b>Prevents removing from an out-of-bounds location</b> → Print "Error: Invalid kennel position." and return `null`.
- <b>Prevents removing a dog from an empty space</b> → Print "Error: No dog to remove at this position." and return `null`.
- <b>Successfully removes a dog</b> → Store the removed `Dog` in a temporary variable, set its space to `null`, and return the removed `Dog`.

### 4. Display Kennel Layout
```java
public void displayKennel()
```
- <b>Prints a grid showing dog names in each spot</b>.
- <b>Empty spaces should display</b> "---" or "Empty".
- <b>If the kennel is empty</b>, print:
  ```java
  The kennel is empty.
  ```
<b>Example Output:</b>
```java
Lassie      Max        Empty
Fluffy      Empty      Rover
```
### 5. Get Available Spots
```java
public void getAvailableSpots()
```
- <b>Displays all available kennel spaces (row and column)</b>.
- <b>If the kennel is full</b>, print:
```java
No available spots.
```
- <b>If empty</b>, print:
```java
The kennel is empty.
```
### 6.  Filter by Championship Wins
```java
public ArrayList<Dog> filterByChampionships(int num)
```
<b>Returns an `ArrayList<Dog>` of all dogs with `num` or more championship wins</b>.
<b>If no dogs meet the criteria</b>, return `null`.
<b>If the kennel is empty</b>, return `null`.

### 7.  Filter by Weight
```java
public ArrayList<Dog> filterByWeight(int min, int max)
```

<b>Returns an ArrayList<Dog> of all dogs weighing between `min` and `max` (inclusive)</b>.
<b>If no dogs meet the criteria</b>, return `null`.
<b>If the kennel is empty</b>, return `null`.

### 8.  Cound Dogs by Breed
```java
public void countByBreed()
```
<b>Counts the number of each breed in the kennel by iterating through all the dogs in the kennel</b>.
<b>If the kennel is empty</b>, print
```java
The kennel is empty. No breeds to count.
```
<b>Otherwise, display breed counts:</b>
```java
Breed Counts in the Kennel:
Labrador: 3
Poodle: 1
Bulldog: 1
Beagle: 1
Golden Retriever: 0
```
### Testing & Edge Cases
You should test the following cases:
- <b>Edge Case #1: Empty Kennel</b>
  -- Try running countByBreed(), displayKennel(), getAvailableSpots(), and filterByChampionships() in an empty kennel.
- <b>Edge Case #2: Adding a Dog to an Occupied Space</b>
  -- Try adding a second dog to a filled space. It should print an error and return `false`.
- <b>Edge Case #3: Removing from an Empty Space</b>
  -- Try removing a dog from an already empty spot. It should print an error and return `null`.
- <b>Edge Case #4: Out-of-Bounds Errors</b>
 -- Try adding or removing a dog using invalid row/column indices. It should print an error message.
- <b>Edge Case #5: Filtering with No Matches</b>
  --Try filtering by championships or weight when no dogs meet the criteria. The method should return `null`.

### Final Notes
- You need to document all of your methods, including description, preconditions and postconditions.  Note - the edge cases above give hints as to the pre and post conditions.
- Be sure to test these cases.  My tester code will test these cases and you will not get credit for the method if it fails these test cases.
