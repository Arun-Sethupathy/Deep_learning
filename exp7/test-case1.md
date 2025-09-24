import pandas as pd
input_sentences = [
    "How are you?",
    "I love coding."
]
predicted_outputs = [
    "तुम कैसे हो?",
    "मुझे कोडिंग पसंद है।"
]
correct = ["Y", "Y"]
df = pd.DataFrame({
    "Input Sentence": input_sentences,
    "Predicted Output (Hindi)": predicted_outputs,
    "Correct (Y/N)": correct
})
print(df.to_string(index=False))

output:
<img width="482" height="85" alt="Screenshot 2025-09-24 101600" src="https://github.com/user-attachments/assets/51592fc4-c8ca-4cdc-b277-3d7bb4052574" />
