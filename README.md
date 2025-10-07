# Search-Algorithms-in-C-Plus-Plus

Aim: To study different searching techniques in C++ and implement programs to search for elements in an array.

Tools Used: VS Code or Programiz online compiler.

# Theory

# Search Algorithms in C++
Search algorithms are techniques used to find a specific element or value within a data structure, such as an array, list, or database. In C++, search algorithms are commonly classified into linear search and binary search. Linear search checks each element sequentially until the desired value is found or the end of the list is reached. It is simple but inefficient for large datasets, with a time complexity of O(n). Binary search works on sorted arrays by repeatedly dividing the search interval in half, reducing the search space efficiently with a time complexity of O(log n). Other search techniques include jump search, interpolation search, and exponential search, each with different use-cases and efficiencies. Search algorithms are fundamental in data retrieval, database management, and problem-solving in programming, and C++ provides the flexibility to implement them either manually or using STL functions like find() or binary_search().

## Types of Search Algorithms
->Search algorithms are used to find a specific element in a dataset. The three common types are:

1. **Linear Search –** Also called sequential search, it checks each element in the array or list one by one until the desired element is found or the end is reached. It works on both sorted and unsorted data, with a time complexity of O(n).

2. **Sequential Search –** Essentially the same as linear search. Each element is examined in sequence, making it simple but less efficient for large datasets.

3. **Binary Search –** This search works on sorted arrays only. It repeatedly divides the search interval in half, comparing the middle element with the target. If the target is smaller, it searches the left half; if larger, the right half. Its time complexity is O(log n), making it much faster than linear search for large datasets.

These search methods are fundamental in C++ programming for data retrieval, array processing, and problem-solving.

# Program-1: Linear Search
This C++ program demonstrates the linear (or sequential) search algorithm using a vector. The SearchAlgorithms class contains a function linearSearch() which takes a vector and a key value as inputs. The function iterates through each element of the vector sequentially, comparing it with the key. If a match is found, it prints the index of the element and exits the function. If the key is not found after checking all elements, it prints “Element not found.”

In the main() function, a vector of integers {1, 5, 2, 6, 3, 9, 0} is created, and the linearSearch() function is called to search for the value 10. Since 10 is not present in the vector, the program outputs “Element not found.” This program illustrates the simplicity and functionality of linear search, which works on both sorted and unsorted data, with a time complexity of O(n) in the worst case.

--> Algorithm:

1. Start
2. Initialize a vector or array of size n with elements.
3. Input the element to be searched, key.
4. Set a flag variable to indicate whether the element is found.
5. For each element in the vector (from index 0 to n-1):
  --Compare the current element with key.
  --If the element matches key:
    -Print the index of the element.
    -Exit the loop.
  --Else, continue to the next element.
6. If the element is not found after checking all elements:
  --Print “Element not found.”
7. End

# Program-2: Sequential Search
This C++ program demonstrates the linear (sequential) search algorithm. The program first takes the number of elements n from the user and stores the elements in an array. It then asks the user to input a key element to search for. The program iterates through each element of the array sequentially and compares it with the key. If a match is found, it prints the index of the element and stops the search. If the key is not found after checking all elements, it displays “Element not found in the array.”

This approach illustrates the simplicity of linear search, which works on both sorted and unsorted arrays, and has a time complexity of O(n) in the worst case. It is a fundamental search technique used in data retrieval and array processing.

--> Algorithm:

1. Start
2. Input the number of elements, n.
3. Create an array of size n and input all elements.
4. Input the element to be searched, key.
5. Initialize a boolean variable found = false.
6. For each element in the array (from index 0 to n-1):
  --If the current element equals key:
    -Print the index of the element.
    -Set found = true.
    -Break the loop.
7. If found is still false after checking all elements:
  --Print “Element not found in the array.”
8. End

# Program-3: Binary Search
This C++ program demonstrates the binary search algorithm, which is an efficient method to find an element in a sorted array. The binarySearch() function takes the array, its size, and the value to search as inputs. It uses two pointers, left and right, to define the current search range. The middle element is calculated, and if it matches the target value, its index is returned. If the middle element is smaller than the target, the search continues in the right half of the array; if larger, it continues in the left half. This process repeats until the element is found or the search range becomes empty.

In the main() function, the program takes a sorted array from the user and the value to search. It calls binarySearch() and prints the index if the element is found or displays a message if not. Binary search is much faster than linear search, with a time complexity of O(log n), but it requires the array to be sorted. It is widely used in searching, databases, and algorithm optimization.

--> Algorithm:

1. Start
2. Input the number of elements size and create a sorted array of that size.
3. Input all elements of the array in ascending order.
4. Input the value to be searched, val.
5. Initialize two pointers: left = 0 and right = size - 1.
6. While left <= right:
  --Calculate mid = left + (right - left) / 2.
  --If arr[mid] == val, return mid (element found).
  --Else if arr[mid] < val, set left = mid + 1 (search in right half).
  --Else, set right = mid - 1 (search in left half).
7. If the element is not found, return -1.
8. Display the result: if -1, print “Element not found”; else, print the index.
9. End

# Conclusion
These programs demonstrate the implementation of search algorithms in C++. The first two programs illustrate linear (sequential) search, where each element is checked one by one until the desired value is found or the end of the array/vector is reached. Linear search works on both sorted and unsorted data, but it can be inefficient for large datasets due to its O(n) time complexity. The third program demonstrates binary search, which works only on sorted arrays and repeatedly divides the search interval in half to locate the element, making it much faster with a time complexity of O(log n). Together, these programs highlight how different search techniques can be applied based on the size and ordering of data, and they form the foundation for efficient data retrieval and problem-solving in C++ programming.
