# PA-2
Second Programming assignment for Advanced Programming and Algorithm

##### NUMBER 1.

The first part of the code creates a random array with the size that the user type in.
After the input, it then normalizes the array. The code aims to subtract the mean of the array from each element and then
divide each element by the show spread out the numbers are. Once finish, the result is a new array whose values are centered around 0. 

```
rows = int(input("Enter number of rows for random array: "))
cols = int(input("Enter number of columns for random array: "))

X = np.random.rand(rows, cols)

mean_X = X.mean()
std_X = X.std()
X_normalized = (X - mean_X) / std_X

np.save('X_normalized.npy', X_normalized)

print("\nRandom array X:\n", X)
print("\nNormalized array X_normalized:\n", X_normalized)
```

##### NUMBER 2

The second part automatically builds a ten by ten grid of the squares of the numbers 1 to 100.
And then it filters out and collects only the squares divisible by three
This code can quickly generate any sequence to reshape it into a matrix and select values based on a condition.

```
A = np.arange(1, 101)**2  
A = A.reshape(10, 10)   

div_by_3 = A[A % 3 == 0]

np.save('div_by_3.npy', div_by_3)

print("\nArray A (10x10 squares):\n", A)
print("\nNumbers divisible by 3:\n", div_by_3)
```
