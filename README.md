# PA-2
Second Programming assignment for Advanced Programming and Algorithm

##### NUMBER 1.

The first part of the code creates a random array with the size that the user type in.
After the input, it then normalizes the array. The code aims to subtract the mean of the array from each element and then
divide each element by the show spread out the numbers are. Once finish, the result is a new array whose values are centered around 0. 

```Python
rows = int(input("Enter number of rows for random array: "))  # Asks the user how many rows the array should have and converts it to an integer.
cols = int(input("Enter number of columns for random array: "))  # Asks the user how many columns the array should have and converts it to an integer.

X = np.random.rand(rows, cols)  # Creates a random array X with values between 0 and 1 using the given rows and columns.

mean_X = X.mean()  # Calculates the mean (average) of all values in X.
std_X = X.std()  # Calculates the standard deviation of all values in X.
X_normalized = (X - mean_X) / std_X  # Normalizes X so that its values have mean 0 and standard deviation 1.

np.save('X_normalized.npy', X_normalized)  # Saves the normalized array to a file named 'X_normalized.npy'.

print("\nRandom array X:\n", X)  # Prints the randomly generated array X.
print("\nNormalized array X_normalized:\n", X_normalized)  # Prints the normalized array X_normalized.

```

##### NUMBER 2

The second part automatically builds a ten by ten grid of the squares of the numbers 1 to 100.
And then it filters out and collects only the squares divisible by three
This code can quickly generate any sequence to reshape it into a matrix and select values based on a condition.

```Python
A = np.arange(1, 101)**2  # Creates an array of squares of numbers from 1 to 100.
A = A.reshape(10, 10)  # Reshapes the array into a 10x10 matrix.

div_by_3 = A[A % 3 == 0]  # Extracts all numbers from A that are divisible by 3.

np.save('div_by_3.npy', div_by_3)  # Saves the numbers divisible by 3 into a file named 'div_by_3.npy'.

print("\nArray A (10x10 squares):\n", A)  # Prints the full 10x10 array A.
print("\nNumbers divisible by 3:\n", div_by_3)  # Prints only the numbers divisible by 3.

```
Version 2
