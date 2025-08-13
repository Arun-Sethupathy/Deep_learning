#exp1 test case 2
import numpy as np

weights = np.array([0.5, 0.5])
bias = -0.2

def perceptron(x):
    summation = np.dot(x, weights) + bias
    return 1 if summation >= 0 else 0

inputs = np.array([[0,0], [0,1], [1,0], [1,1]])
expected_outputs = np.array([0, 1, 1, 0])

print(f"{'Test Input (X)':<15} {'Actual Output':<20} {'Expected':<10} {'Remarks'}")

for i, x in enumerate(inputs):
    output = perceptron(x)
    may_fail = (list(x) in [[0,1], [1,0]])
    actual_display = "0 or 1 (varies)" if may_fail else str(output)
    remark = "May fail" if may_fail else "Correct"
    print(f"{str(list(x)):<15} {actual_display:<20} {expected_outputs[i]:<10} {remark}")
    OUTPUT:
    <img width="482" height="95" alt="Screenshot 2025-08-13 103451" src="https://github.com/user-attachments/assets/7cdb2bc3-66cc-48b1-bf80-7a1087c8529c" />
