---

# **Custom Python Iterator: Counter Class**  

## **Overview**  
**`Counter`** is a Python class that implements a custom iterator. It generates numbers within a specified range, using a given step value. The iterator starts from the defined starting value, increments by the step value, and stops when it reaches or exceeds the end value.

## **Features**  
- Custom iteration with configurable **start**, **end**, and **step** values.  
- Generates numbers **one at a time** within the defined range.
  
## **Usage**  

```python
class Counter:
    def __init__(self, start, end, step=1):
        self.start = start
        self.end = end
        self.step = step
    
    def __iter__(self):
        return self
    
    def __next__(self):
        if self.start < self.end:
            num = self.start
            self.start += self.step
            return num
        raise StopIteration

# Example usage
for i in Counter(0, 50, 5):
    print(i)
```

### **Example Output:**  
```
0
5
10
15
20
25
30
35
40
45
```

## **How to Run**  
1. Clone this repository:
    ```bash
    git clone https://github.com/YOUR_USERNAME/Custom_Python_Iterator.git
    ```

2. Navigate to the project directory:
    ```bash
    cd Custom_Python_Iterator
    ```

3. Run the script:
    ```bash
    python counter.py
    ```

## **Contributing**  
Feel free to **fork** this repository, **make improvements**, and **submit pull requests**.

## **License**  
This project is licensed under the **MIT License**.
