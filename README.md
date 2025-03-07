# Custom_Python_Iterator

Overview
Counter is a Python class that implements a custom iterator. It generates numbers in a specified range with a given step. The iterator starts from a given value, increments by a specified step, and stops when it reaches or exceeds the end value.

Features
Custom iteration with configurable start, end, and step values.
Generates numbers within the defined range, one at a time.
Usage
python
Copy
Edit
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
Example
Output:
Copy
Edit
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
Contributing
Feel free to fork this repository, improve it, and submit pull requests.

License
This project is licensed under the MIT License.

