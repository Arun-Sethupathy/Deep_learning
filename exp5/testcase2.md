# Define data
reviews = [
    "I loved the movie, fantastic!",
    "Worst film ever, boring.",
    "It was okay, not great."
]

actual_sentiments = ["Positive", "Negative", "Neutral"]
predicted_sentiments = ["Positive", "Negative", "Positive"]
correct = ["Y", "Y", "N"]

# Print the table header
print(f'{"Review Text":<35} {"Actual Sentiment":<15} {"Predicted Sentiment":<20} {"Correct (Y/N)"}')

# Print the rows
for i in range(len(reviews)):
    print(f'"{reviews[i]:<30}" {actual_sentiments[i]:<15} {predicted_sentiments[i]:<20} {correct[i]}')

output:

<img width="678" height="96" alt="Screenshot 2025-09-03 120337" src="https://github.com/user-attachments/assets/49b84288-a99a-4c47-adb7-eb0506b14d9a" />
