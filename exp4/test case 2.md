#exp4 test case 2
test_cases = [
    {"input": "Deep learning is", "predicted": "amazing", "expected": "amazing"},
    {"input": "Deep learning builds", "predicted": "intelligent", "expected": "intelligent"},
    {"input": "Intelligent systems can", "predicted": "learn", "expected": "intelligence"}  # mismatch
]

print(f"{'Input Text':<30}{'Predicted Word':<15}{'Correct (Y/N)':<15}")
print("-" * 60)

for case in test_cases:
    correct = "Y" if case["predicted"] == case["expected"] else "N"
    print(f"{case['input']:<30}{case['predicted']:<15}{correct:<15}")

    output:
    <img width="449" height="108" alt="Screenshot 2025-09-03 094026" src="https://github.com/user-attachments/assets/cefc4f13-86dd-4f3c-8c0b-4e2da52c9209" />
