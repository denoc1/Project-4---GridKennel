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

- Initializes an empty kennel with the given number of rows and columns.
- All spaces in kennel should start as null.
```
### 2.  Add a Dog

```java
public boolean addDog(Dog dog, int row, int col)
```

- <b>Prevents adding a dog outside of bounds</b> → Print "Error: Invalid kennel position." and return <i>false</i>.
- <b>Prevents overwriting an occupied space</b> → Print "Error: This kennel spot is already occupied." and return <i>false</i>.
- <b>Successfully adds a dog</b> → Place the Dog object in the array and return true.

### 3.  Remove a Dog
```java
public Dog removeDog(int row, int col)
```
- <b>Prevents removing from an out-of-bounds location</b> → Print "Error: Invalid kennel position." and return <i>null</i>.
- <b>Prevents removing a dog from an empty space</b> → Print "Error: No dog to remove at this position." and return <i>null</i>.
- <b>Successfully removes a dog</b> → Store the removed Dog in a temporary variable, set its space to null, and return the removed Dog.

### 4. Get Available Spots
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

