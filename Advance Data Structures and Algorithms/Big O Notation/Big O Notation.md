# ** Big O Notation

#### **Big O Notation**

    --> Time Complexity ( Resources )
    --> Space Complexity ( Storage )


## **Time Complexity**

* The **running time** of an algorithm takes increases with the **number of inputs grows**. 
 

### **O(1) - Constatnt Time Complexity**

> No mattes how long the inputs are time takes for the algorithm is same.

Example I

    public void printFirst(int[] number){
        System.out.printFirst(number[0]);
    } 
    // Number of inputs in the number array is no matter. We are just printing the first value.


### **O(n) - Linear Time Complexity**

> Algorithm's running time is incrreasing with the number of inputs insert.

Example I

    public void printArray(int[] number){
        System.out.println(number[i]);
    }
    // Running time increases with the number of inputs in the number[] array.


### **O(n²) - Quadratic Time Complexity**

> Algorithm's running time grows with the square of input size

Example I

    public static void printTen() {

        for (int i = 1; i <= 1; i++) { 
            for (int j = 1; j <= 10; j++) {
                System.out.println(j);
            }
        }
    } 
    // Running time increases with the square of the number of inputs because two loops iterate over the input.


### **O(log n) - Logarithmic Time Complexity**

> Algorithm’s running time decreases the problem size by half in each step.

Example I

    public static int find(int[] a, int x) {
        int l = 0, r = a.length - 1;
        while (l <= r) {
            int m = (l + r) / 2;
            if (a[m] == x) return m;
            if (a[m] < x) {
                l = m + 1;
            }else{
                r = m - 1;
            } 
        }
        return -1;
    }
    // Running time grows logarithmically because the search range is reduced by half each iteration.


## **Space Complexity**

* * How much **additional memory** an algorithm needs as the **input size increases**.


### **O(1) - Constatnt Space Complexity**

> Algorithm's space usage remains constant regardless of input size.

Example I

    public void printArray(int[] number){
        for(int i = 0; i < number.length; i++){
            System.out.println(number[i]);
        }
    }
    // Space usage does not grow with the size of number[] array


### **O(n) - Linear Space Complexity**

> Algorithm’s **space usage grows** linearly with the **size of the input** array.

    public void copyArray(int[] number){
        int[] arr = new int[number.length];  // Extra space grows with number[] size
        for(int i = 0; i < number.length; i++){
            arr[i] = number[i];
        }
    }
    // Space usage grows linearly with number[] size    



# **Algorithms Cases**

    > Best Case
    > Average Case
    > Worst Case (O - Big O)


## ** Best Case  (Ω - Omega)
 
> The minimum time an algorithm takes for the best possible input.

Example I 

    Searching number 10
        +----+----+----+----+----+
        | 10 | 20 | 30 | 40 | 50 |   // Searching for the first element in an array
        +----+----+----+----+----+


## ** Average Case  (Θ - Theta)

> The expected time an algorithm takes on average across all inputs.

Example I 

    Searching number 10
        +----+----+----+----+----+
        | 30 | 20 | 10 | 40 | 50 |   // Searching for an element randomly in an array
        +----+----+----+----+----+


## ** Worst Case  (O - Big O)

> The maximum time an algorithm could take.

Example I 

    Searching number 10
        +----+----+----+----+----+
        | 40 | 10 | 50 | 20 | 10 |   // Searching for an element at the end of the array or not present at all
        +----+----+----+----+----+



## **🔍 Searching Algorithms

### ** Linear Search**

> Traverse the array one by one until the element is found.

Example I

    +----+----+----+----+----+
    | 10 | 20 | 30 | 40 | 50 |
    +----+----+----+----+----+
    i ->  ^    ^    ^    ^    ^
    Step: 1    2    3    4    5
    Found at index 3 ✅

    Note: Traverse each element until the target is found. Worst case → last element → O(n) time.


## ** Binary Search**

> Works on sorted arrays.
> Check the middle element if it’s smaller than target, search right half if bigger, search left half.

Example I

    +----+----+----+----+----+
    | 10 | 20 | 30 | 40 | 50 |
    +----+----+----+----+----+
    Step 1: mid -> 30 ❌ (search right)
    Right half:
    +----+----+
    | 40 | 50 |
    +----+----+
    Step 2: mid -> 40 ✅ Found!

    Note: Each step halves the search space → O(log n) time.

