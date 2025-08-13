#test case exp no:2
import pandas as pd
import numpy as np
true_labels = ["T-shirt", "Trouser", "Pullover", "Sneaker"]
predicted_labels = ["T-shirt", "Dress", "Pullover", "Ankle boot"]
df = pd.DataFrame({
    "Input Image": true_labels,
    "True Label": true_labels,
    "Predicted Label": predicted_labels
})
df["Correct (Y/N)"] = np.where(df["True Label"] == df["Predicted Label"], "Y", "N")
print(df)

OUTPUT:
<img width="420" height="109" alt="Screenshot 2025-08-13 120239" src="https://github.com/user-attachments/assets/62d192c9-b74a-49a4-999b-aa2b9bd4ffa0" />
