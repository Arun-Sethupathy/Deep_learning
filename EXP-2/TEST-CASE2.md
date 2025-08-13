#TEST CASE 2 EXP NO.2
import pandas as pd
import numpy as np
data = [
    ["Image of 7", 7, 7],
    ["Image of 3", 3, 3],
    ["Image of 8", 8, 8],
    ["Image of 1", 1, 2]
]
df = pd.DataFrame(data, columns=["Input Digit Image", "Expected Label", "Model Output"])
df["Correct (Y/N)"] = np.where(df["Expected Label"] == df["Model Output"], "Y", "N")
print(df)

OUTPUT:
<img width="481" height="115" alt="Screenshot 2025-08-13 120343" src="https://github.com/user-attachments/assets/e2c3419d-786a-498b-8c35-fd32a01c972b" />
